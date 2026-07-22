---
name: extract-documents
description: Extracts structured data from batches of invoices, receipts, statements, and similar documents (PDF, photo, scan) into a validated table — with totals checks, deduplication, and explicit flags for unreadable fields. Use when asked to "extract data from these invoices", "receipts to a spreadsheet", "parse these PDFs", "вытащи данные из счетов", "чеки в таблицу".
---

# Extract Documents

## Overview

A folder of financial or form-like documents → one clean table plus an exceptions list. The rule that makes this trustworthy: never guess a value — an unreadable field is reported, not invented.

## When to Use

- Invoices, receipts, bank/card statements, purchase orders, forms — any repetitive document type arriving as PDF/scan/photo
- NOT for: single-document Q&A (just read it), or contracts/legal analysis (different task than field extraction)

## Process

1. **Inventory the batch.** List the files, note formats and count. If mixed document types, group them — each type gets its own schema and table.
2. **Fix the schema before extracting.** For invoices the default is: file, vendor, invoice number, issue date, due date, currency, net, tax, gross, line-item summary. Confirm extra fields the user needs (project codes, categories). Dates → ISO 8601, amounts → plain decimals, one currency column — no `$1 234,56` strings.
3. **Extract file by file** using the best available reading path (native PDF text, OCR, or vision on images). Per file record a confidence note. Rules:
   - Unreadable or missing field → `UNREADABLE` / `MISSING`, never a guess
   - Ambiguous date format (03/04/2025) → resolve from context (due date after issue date, locale) or flag
   - Keep the source filename on every row — traceability beats elegance
4. **Validate arithmetic.** net + tax = gross per row (respect rounding to 2 decimals); line items sum to net where present. Mismatch → flag the row, keep the document's own stated totals (do not "fix" them).
5. **Deduplicate.** Same vendor + invoice number + gross = duplicate; same file content twice = duplicate. List dropped duplicates.
6. **Deliver:**
   - `extracted.csv` (or the user's target sheet) with all clean rows
   - **Exceptions section:** per problem file — what failed and what a human should check
   - Totals line: documents in, rows out, duplicates dropped, exceptions count, sum of gross per currency

## Verification

- [ ] Row count + duplicates + exceptions = input file count
- [ ] Every flagged row explains why; zero silently-guessed values
- [ ] Arithmetic check ran on every row; failures are in exceptions
- [ ] Amounts and dates are machine-parseable (no locale formatting)

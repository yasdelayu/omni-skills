---
name: finance-report
description: Builds a periodic finance report from transactions, statements, or expense exports — categorized spend, period-over-period trends, anomalies, and recurring-subscription tracking, with arithmetic that reconciles. Use when asked for a "monthly financial report", "categorize my expenses", "where did the money go", "финансовый отчёт", "разбери расходы".
---

# Finance Report

## Overview

Raw transactions → a report where every number reconciles and surprises are surfaced. Bookkeeping analytics only: this skill describes what happened to the money; it never gives investment advice.

## When to Use

- Personal or business spend reviews from CSV exports, bank statements, or accounting-tool data reachable via available tools
- NOT for: investment recommendations, tax advice, or forecasting presented as certainty. Extraction from document scans is the extract-documents skill's job; this skill starts once transactions are tabular

## Process

1. **Normalize the input.** One table: date, description, amount (signed), currency, account. Multiple currencies → separate subtotals; convert only if the user provides rates or approves a source, and label converted figures as approximate.
2. **Categorize every transaction.** Start from the user's category set if one exists (previous reports, accounting codes); otherwise propose a sensible set (10–15 categories max) and apply it. Rules: a transaction gets exactly one category; genuinely unclear → `Uncategorized` (target: under 5% of total volume — above that, ask the user about the top unclear merchants instead of guessing).
3. **Reconcile before analyzing.** Sum of categorized = sum of input; income − spend = net for the period. If the numbers don't close, find the gap now — a report built on a leaky base is fiction.
4. **Analyze:**
   - Spend by category, sorted, with share of total and delta vs. previous period (when prior data exists)
   - **Recurring items:** same merchant + similar amount at regular intervals → subscription list with monthly total and any price creep
   - **Anomalies:** duplicates (same merchant, amount, date), outliers ≥3× the category's typical transaction, first-ever merchants above a notable threshold
   - Top 10 merchants by volume
5. **Report** in Markdown: headline (income, spend, net, biggest mover), category table, subscriptions, anomalies with the underlying rows, and a short neutral observations section — facts ("delivery spend doubled"), not lectures ("you should cook more").

## Verification

- [ ] Category totals sum exactly to input total; net figure reconciles
- [ ] Uncategorized under 5% or explicitly discussed with the user
- [ ] Every anomaly cites its underlying transaction rows
- [ ] Zero investment/tax advice — descriptive statements only

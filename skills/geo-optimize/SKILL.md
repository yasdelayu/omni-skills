---
name: geo-optimize
description: Optimizes an article or page for citation by AI search engines (AI Overviews, ChatGPT, Perplexity, Yandex Neuro) — answer-first opening, self-contained quotable blocks, visible FAQ matching schema, sourced claims, freshness markers. Use when asked to "optimize for AI search", "GEO", "make AI engines cite this", "оптимизируй под нейропоиск", "чтобы ChatGPT ссылался".
---

# GEO Optimize

## Overview

AI engines don't rank pages — they lift passages. A page gets cited when it contains self-contained, quotable, sourced blocks an engine can extract without the surrounding context. This skill restructures content for that, on top of (not instead of) classic SEO.

## When to Use

- An existing draft or published page that should surface in AI-generated answers
- Writing guidance for new content with AI citation as a goal
- NOT for: keyword-ranking work in classic SERPs (that's the seo-article skill's territory), or manipulating engines with hidden/schema-only content — visibility parity is a hard rule here

## Process

1. **Identify the queries** this page should be the answer to (3–7, including question-phrased ones). Every optimization below is checked against them.
2. **Answer-first opening.** The first paragraph (≤100 words) must directly answer the primary query — extractable as a standalone answer with zero throat-clearing. The "what this article will cover" intro is the first thing to die.
3. **Make blocks self-contained.** Restructure so key passages (definitions, verdicts, how-to summaries, comparisons) work when lifted out alone:
   - 40–80 words per block, one thesis each
   - No dangling references — "as mentioned above", "this approach" (which?), pronouns pointing outside the block
   - Headings that state the answer's topic plainly; the H2/H3 outline alone should read as a table of contents an engine can navigate
4. **Make claims citable.** Numbers get a named source and a date; "studies show" without a study is either sourced or deleted. Add 2–4 genuinely quotable sentences: concrete fact + entity + number/date, phrased so quoting them requires attribution to make sense.
5. **Visible FAQ.** 3–7 question-phrased H3s matching real query formulations, each answered in the first sentence, nuance after. If FAQ schema (JSON-LD) is added, it mirrors the visible text exactly — schema-only content is deception and a penalty risk.
6. **Entity and freshness hygiene:** the subject is named unambiguously (product + maker + category) at least once instead of pronoun chains; visible date; versions/prices marked with "as of" dates.
7. **Deliver:** the restructured content (or a concrete edit list for a live page), plus a check table — query → the exact block that now answers it.

## Verification

- [ ] First paragraph answers the primary query standalone
- [ ] Each target query maps to one self-contained block (the check table proves it)
- [ ] Zero unsourced statistics; quotable lines carry entity + specifics
- [ ] Any schema mirrors visible content 1:1
- [ ] No dangling references inside key blocks — lift-out test passed on 3 random blocks

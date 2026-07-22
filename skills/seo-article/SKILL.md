---
name: seo-article
description: Writes a search-optimized article from a target keyword — SERP reconnaissance, intent match, gap-driven outline, draft, and an on-page SEO pass with title/meta/schema. Use when asked to "write an SEO article", "blog post for keyword X", "rank for...", "SEO-статья", "статья под ключевик".
---

# SEO Article

## Overview

Keyword → article that earns its ranking: covers what the SERP rewards, adds what competitors miss, and ships with clean on-page metadata. Prevents the default failure — generic content written blind to what already ranks.

## When to Use

- Content pieces targeting a known search query or topic cluster
- NOT for: technical SEO audits of a site (crawlability, CWV — different discipline), or content where search traffic isn't the goal

## Process

1. **SERP recon.** Search the target keyword; open the top 5–8 results. Record: dominant intent (informational / commercial / transactional), content format that ranks (listicle, guide, comparison), typical depth, subtopics everyone covers, and — most important — questions or angles nobody covers well. Check "People also ask" style questions.
2. **Match intent or stop.** If the SERP is all product pages and the user wants a blog post (or vice versa), flag the mismatch before writing.
3. **Outline from gaps.** H2/H3 structure that covers the table-stakes subtopics plus 1–2 gap sections competitors lack. Each H2 maps to something a searcher actually wants answered. Get outline approval if the user is available; otherwise proceed and note assumptions.
4. **Draft.** Rules:
   - Answer the query's core question within the first 150 words
   - Keyword in H1, first paragraph, and naturally in 2–3 subheads — no stuffing
   - Specifics over filler: numbers, examples, steps, screenshots-to-add markers. Cut every sentence that could appear in any article on any topic
   - Short paragraphs (≤4 lines), scannable subheads, one table or list where it genuinely compresses information
5. **On-page pass.** Deliver with the article:
   - Title tag ≤60 chars (keyword near front) + meta description ≤155 chars with a reason to click
   - URL slug suggestion (short, hyphenated, keyword-bearing)
   - FAQ block (3–5 real questions from recon) + matching FAQPage JSON-LD snippet
   - 3–5 internal link anchors to suggest (placeholders if site structure unknown)
6. **Deliver** as one Markdown file: metadata block on top, article body, FAQ + schema at the end.

## Verification

- [ ] Recon notes list ≥5 analyzed URLs and at least one named gap the article fills
- [ ] Intent of the article matches the observed SERP intent
- [ ] Title ≤60 chars, meta ≤155 chars, keyword in H1 and first paragraph
- [ ] No section is generic filler — each H2 answers a real searcher question

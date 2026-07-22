---
name: news-digest
description: Compiles a deduplicated, cited news digest on a topic or source list for a given period — multi-query sweep, one entry per story, ranked by impact, every item linked and dated. Use when asked for "news digest", "what happened in X this week", "daily/weekly summary of...", "дайджест новостей", "что нового в...".
---

# News Digest

## Overview

Topic → digest where each story appears once, says why it matters, and links to a source. Prevents the two default failures: the same event repeated from five outlets, and summaries with no links.

## When to Use

- Recurring or one-off briefings: industry news, competitor news, tech/regulatory updates for a period
- NOT for: deep research on a single question (use a research workflow), or real-time breaking-news tracking

## Process

1. **Fix scope.** Topic, period (default: last 7 days), audience, output language, and item budget (default: 5–10). If the user has preferred sources, they go first.
2. **Sweep with 3–5 different queries**, not one: the topic itself, key company/product names, and the topic in the audience's language if different. Use news-oriented search where available. Collect candidates with URL + publication date.
3. **Filter hard.** Drop: items outside the period, paywalled items you couldn't actually read, press-release rewrites with no substance, and anything whose date you can't establish.
4. **Deduplicate by event, not by URL.** Five articles about one funding round = one digest item; keep the most authoritative or original source as the primary link, others as "also covered by" if useful.
5. **Rank by impact for the stated audience**, not by recency. Lead with what changes decisions.
6. **Write each item as:** bold one-line headline (your words, not the outlet's clickbait) → 2–3 sentences: what happened + why it matters to this audience → source link with date. No item without a link.
7. **Close with a "watching" line** (optional): 1–2 developing stories worth tracking next period.

## Verification

- [ ] Every item has a working source link and a date inside the period
- [ ] No two items describe the same event
- [ ] "Why it matters" present in every item — a digest entry that only restates the headline is cut
- [ ] Item count within budget; if fewer real stories than budget, say so instead of padding

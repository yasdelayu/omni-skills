---
name: review-sentiment
description: Gathers customer reviews of a product or company across public platforms, classifies sentiment, clusters recurring themes with quoted evidence, and produces an action-ranked report. Use when asked to "analyze reviews", "what do customers say about X", "sentiment analysis of feedback", "анализ отзывов", "что пишут о...".
---

# Review Sentiment

## Overview

Product name → evidence-backed picture of what customers praise and complain about, ranked by what to fix first. Every theme is proven with quoted reviews — no vibes-based summaries.

## When to Use

- Understanding reception of a product/service/company (own or competitor's) from public reviews
- NOT for: analyzing a private review export the user provides (skip step 2 — go straight to classification), or platforms behind login

## Process

1. **Fix scope.** Product/company, platforms if the user cares (default: sweep what's public — marketplaces, app stores, Google Maps reviews, Trustpilot-style sites, Reddit and niche forums), period, and language(s).
2. **Sweep multiple surfaces** via web search and page fetches — minimum 3 distinct platforms unless the product only lives on one. Aim for ≥30 reviews before analyzing; if fewer exist, report the count honestly and lower confidence accordingly.
3. **Collect verbatim.** For each review: quote (trimmed OK, meaning intact), platform, date if visible, rating if visible, link to the page it appears on. Never paraphrase at collection stage and never invent quotes.
4. **Classify and cluster.** Sentiment per review (positive / negative / mixed), then cluster into named themes ("shipping delays", "support response time", "battery life"). A theme needs ≥2 independent reviews; singletons go to "one-off mentions".
5. **Report:**
   - Headline verdict: overall sentiment split (counts, not just percentages) and the single dominant impression
   - Top 3–5 complaint themes and top 3 praise themes, each with count, 1–2 representative quotes with links, and platform spread
   - Trend note if dates allow (getting better/worse)
   - Recommended actions ranked by frequency × severity — a rare-but-fatal theme (data loss, fraud accusations) outranks a common mild one
6. **Flag review credibility issues** if seen: bursts of same-day 5-star reviews, template wording, incentivized-review markers.

## Verification

- [ ] Every theme cites ≥2 quoted reviews with working links
- [ ] Sentiment split adds up to the total collected count
- [ ] All quotes are verbatim from sources — spot-check two against their links
- [ ] Actions ranked with reasoning, not listed flat

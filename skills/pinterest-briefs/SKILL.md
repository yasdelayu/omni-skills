---
name: pinterest-briefs
description: Researches a Pinterest niche from public pins and produces evidence-backed content opportunity briefs — recurring themes with counts, gaps, and production-ready briefs where every claim cites collected pins. Use when asked for "Pinterest content ideas", "what works in my niche on Pinterest", "Pinterest research", "контент-план для Pinterest", "что пинить".
---

# Pinterest Briefs

## Overview

Niche in, five production-ready content briefs out — built strictly from what public pins show, not from trend folklore. The honesty contract: no search-volume or growth claims (that data isn't observable from pins); every finding cites the pins that prove it; too little evidence halts the run instead of thinning the soup.

## When to Use

- Recurring (weekly works well) or one-off niche research for Pinterest content planning
- NOT for: platforms this evidence model doesn't fit (Pinterest is search-driven and evergreen — TikTok/Instagram research needs different signals), posting/scheduling, or anything requiring login-walled data

## Process

1. **Fix the research frame.** One niche + 3–5 exact search phrases a Pinner would type (get them from the user or derive from the niche and confirm). Language and region matter on Pinterest — pin both.
2. **Collect public pins** per phrase via available scrape/search tools (Pinterest search result pages and trends.pinterest.com are public; a scraping tool or MCP helps but plain fetches work). Target 20–100 pins per phrase. Record per pin: title, description snippet, board name if visible, URL.
3. **Gate on evidence volume.** Normalize and dedupe (same pin surfacing under two phrases counts once). **Fewer than 10 usable pins total → halt** and report what was tried — a brief built on 6 pins is fiction with citations.
4. **Build the evidence packet before interpreting.** Deterministic counts, not impressions: recurring words/phrases in titles with frequencies, format markers (how-to, listicle, checklist, before/after, recipe-card style), visible seasonal hooks. This table goes into the deliverable — the analysis must be checkable against it.
5. **Analyze from the packet only:**
   - **Themes:** 3–5 recurring patterns, each with its count and 2–3 example pin URLs
   - **Gaps:** phrases/angles users search where collected results look weak, thin, or stale — stated as "weak coverage in the sample", never as "low competition" (that's a volume claim)
   - Strip anything the packet doesn't support — an insight without citations gets deleted, not softened
6. **Write 5 content briefs**, each: working title in the niche's actual pin language, angle and why the evidence suggests it (theme or gap, cited), format, keywords drawn from collected titles, and a concrete visual direction. Production-ready means a designer/writer could start without asking questions.
7. **Persist for re-runs.** Save pins and briefs (e.g. `pinterest-research/<niche>/YYYY-MM-DD.md` + a pins CSV keyed by pin URL). On the next run, dedupe against saved pins and note what changed since — that's what makes weekly runs compound.

## Verification

- [ ] Evidence gate enforced: ≥10 usable pins or an honest halt report
- [ ] Every theme and gap cites specific collected pins; counts match the packet table
- [ ] Zero search-volume/trend-growth claims anywhere
- [ ] Exactly 5 briefs, each traceable to a cited theme or gap
- [ ] Results persisted with stable keys; re-run dedupes against prior data

---
name: competitor-watch
description: Tracks competitor pricing, features, and changelog pages — fetches tracked URLs, extracts structured facts, diffs against the last saved snapshot, and reports only what changed. Use when asked to "check competitors", "monitor pricing", "what changed on their site", "мониторинг конкурентов", "проверь цены у конкурентов".
---

# Competitor Watch

## Overview

Snapshot-and-diff monitoring of competitor pages, run on demand by an agent. State lives in a plain `competitor-watch/` directory, so any agent with file access and a web fetch tool can run a check.

## When to Use

- Recurring "what did competitors change" checks: pricing, plans, feature lists, changelogs
- NOT for: one-off competitor research (just fetch and summarize), or sub-daily monitoring (use a dedicated monitoring service)

## Process

1. **Locate or create state.** Look for `competitor-watch/` in the working directory. If missing, ask which competitors and URLs to track, then create:

   ```
   competitor-watch/
     targets.json        # [{"name": "Acme", "urls": ["https://acme.com/pricing"]}]
     snapshots/          # <name>.json — last extraction per competitor
     reports/            # YYYY-MM-DD.md — dated change reports
   ```

2. **Fetch every tracked URL** with the available web fetch/scrape tool. If a page fails, record the failure in the report — never silently skip.
3. **Extract structured facts**, not raw HTML: plan names, prices, billing period, limits, notable features, latest changelog entries. Keep the schema stable between runs so diffs are meaningful.
4. **Diff against `snapshots/<name>.json`.** First run for a target = baseline; say so, no changes to report. Otherwise compare field by field: price changes, added/removed plans, added/removed features, new changelog entries.
5. **Write `reports/YYYY-MM-DD.md`** containing only targets with changes (plus fetch failures). Every change shows before → after with the source URL. End with a one-line verdict: what matters most, or "no meaningful changes".
6. **Update snapshots** with the new extraction — after the report is written.

## Verification

- [ ] Every reported change has explicit before → after values and a source URL
- [ ] Baselines are labeled as baselines, not reported as "changes"
- [ ] Failed fetches appear in the report
- [ ] Snapshots on disk now match today's extraction

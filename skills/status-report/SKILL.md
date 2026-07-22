---
name: status-report
description: Assembles a stakeholder status report from real work artifacts — task trackers, git history, meeting notes, chat threads — into done/in-progress/blocked/risks/next, with every claim traceable to a source. Use when asked for a "status update", "weekly report", "what's the state of the project", "статус проекта", "отчёт за неделю".
---

# Status Report

## Overview

Evidence in, status out. The report is assembled from what the artifacts show, not from optimism — a blocker named on time is the whole reason stakeholders read these.

## When to Use

- Recurring project/sprint/weekly reports, or an on-demand "where are we" for a stakeholder
- NOT for: personal timesheets, or projects where the agent has access to zero artifacts (then it's dictation, not assembly — just ask the user what to write)

## Process

1. **Fix scope and audience.** Which project, what period, who reads it (exec = shorter and risk-first; team = fuller). Find the previous report if one exists — "planned last week" vs. "done this week" is the honesty backbone.
2. **Gather evidence** from every reachable source: task tracker state changes, git log/merged PRs for the period, meeting notes, decision docs, chat announcements. Note sources you *couldn't* reach — a report built only on git history should say so.
3. **Reconcile plan vs. fact.** Items promised in the previous report: done, moved, or dropped? Every slipped item appears with a reason — silently vanishing commitments are how trust dies.
4. **Classify into:**
   - **Done** — shipped/completed this period, each with its artifact (PR, released feature, closed task)
   - **In progress** — with % or stage only if the source supports it; no invented percentages
   - **Blocked** — what, since when, who can unblock, what was already tried
   - **Risks** — things trending badly before they're blockers; date-stamp when first raised so repeat risks visibly age
   - **Next period** — commitments, each with an owner
5. **Write it** in the audience's language: headline verdict first (on track / at risk / off track — pick one, with the single biggest reason), then the sections, total ≤1 page. Numbers over adjectives: "closed 14 of 20 planned" beats "good progress".
6. **Store it** (e.g. `reports/status-YYYY-MM-DD.md`) so the next run has a baseline.

## Verification

- [ ] Every "done" item links to an artifact; every claim traceable
- [ ] All previous-report commitments accounted for — done, moved (with reason), or dropped (with reason)
- [ ] Verdict line present and consistent with the body (no "on track" above three blockers)
- [ ] Unreachable sources disclosed

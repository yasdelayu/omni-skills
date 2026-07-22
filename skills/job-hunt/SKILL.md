---
name: job-hunt
description: Finds job openings matching a candidate's profile, scores each match honestly, tailors resume bullets and a cover letter per role from real experience only, and maintains an application tracking table. Use when asked to "find me jobs", "tailor my resume for this role", "write a cover letter", "найди вакансии", "подгони резюме под вакансию".
---

# Job Hunt

## Overview

Profile + criteria → shortlist of real openings with per-role tailored materials. The integrity rule: tailoring reframes true experience; it never invents skills, titles, or outcomes that aren't the candidate's.

## When to Use

- Job search sprints: discovery, match scoring, resume/cover-letter tailoring, pipeline tracking
- NOT for: auto-submitting applications, or fabricating qualifications to pass filters

## Process

1. **Build the candidate profile.** From the user's resume + a few questions if needed: role targets, seniority, must-haves (remote/geo, salary floor, visa), dealbreakers, and the 5–7 strongest evidence-backed achievements. This profile is the single source of truth for all tailoring.
2. **Search openings** across job boards, company career pages, and search engines reachable with available tools. Fresh postings first (≤2 weeks). Collect: title, company, location/remote, posted date, source URL, key requirements.
3. **Score each opening** against the profile: strong / good / stretch / skip, with the top 2 matching points and the biggest gap named. Be honest about stretches — a candidate applying to everything "strong" that's actually "stretch" burns weeks.
4. **For roles the user picks (or top 5 by default), tailor:**
   - **Resume adjustments** — reorder and reword existing bullets toward the JD's language, surface the relevant achievements, cut irrelevant ones. Output as a diff-style list ("change X → Y"), not a rewritten life
   - **Cover letter** — ≤250 words: why this company specifically (one researched fact), two proof points mapped to their top requirements, plain close. No "I am writing to express my interest"
5. **Maintain `applications.csv`:** company, role, URL, match score, status (found / tailored / applied / interview / rejected / offer), date, next action. Update it on every subsequent run — this skill is re-runnable as the pipeline moves.
6. **Applying is the user's action.** Prepare everything; submit nothing.

## Verification

- [ ] Every listed opening has a source URL and posted date
- [ ] Every tailored bullet traces to something real in the original profile — zero invented experience
- [ ] Match scores include the named gap, not just praise
- [ ] Tracking table updated and consistent with this run's findings

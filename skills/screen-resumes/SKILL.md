---
name: screen-resumes
description: Screens a batch of resumes/CVs against a job description — evidence-based scoring per requirement, ranked shortlist, red flags, and interview questions per candidate. Use when asked to "screen these CVs", "rank candidates", "who fits this role", "отбери резюме", "оцени кандидатов".
---

# Screen Resumes

## Overview

JD + stack of resumes → ranked shortlist where every score is backed by a quote from the resume. Output supports a human decision; it never is the decision.

## When to Use

- First-pass screening of multiple candidates against one role
- NOT for: making the hiring decision, background checks, or judging anything beyond the submitted documents

## Fairness Guardrail (non-negotiable)

Evaluate only job-relevant evidence: skills, experience, outcomes, education where the JD requires it. Ignore — and never mention, score, or infer — age, gender, nationality, ethnicity, religion, family status, photos, or name-based assumptions. Employment gaps are a neutral fact to ask about, not a negative signal.

## Process

1. **Decompose the JD** into an explicit rubric: must-have requirements, nice-to-haves, and disqualifiers. Get the user's confirmation if any requirement is ambiguous. Weight must-haves 2× nice-to-haves by default.
2. **Extract per resume, before scoring:** years of relevant experience, matched skills with the resume line proving each, notable outcomes (numbers > duties), and anything unverifiable-but-claimed.
3. **Score against the rubric.** Per requirement: met / partial / not evident — plus the supporting quote. "Not evident" means the resume doesn't show it, not that the candidate lacks it; say it that way.
4. **Flag honestly, both directions:**
   - Red: contradictory dates, title inflation vs. described duties, keyword-stuffing with no substance
   - Green: strong signals the rubric didn't ask for (open source, relevant side work, unusually concrete outcomes)
5. **Deliver:**
   - Ranked table: candidate, weighted score, must-haves met (n/m), one-line verdict
   - Per candidate: rubric breakdown with quotes, flags, and 2–3 tailored interview questions probing the weakest *evidence* (not the weakest candidate trait)
   - Explicit cut recommendation: interview / maybe / decline-for-this-role — each "decline" tied to a named missing must-have

## Verification

- [ ] Every score cell has a quote or "not evident" — zero unsupported judgments
- [ ] Nothing in the output references protected characteristics
- [ ] Ranking follows the weighted rubric (spot-check top vs. #3)
- [ ] Interview questions target evidence gaps, not generic "tell me about yourself"

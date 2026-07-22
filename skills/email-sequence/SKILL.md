---
name: email-sequence
description: Designs and drafts a multi-email sequence — onboarding, welcome, nurture, or re-engagement — with per-email goals, send triggers, exit conditions, personalization slots, and subject-line variants. Use when asked for a "welcome sequence", "onboarding emails", "nurture campaign", "цепочка писем", "welcome-серия".
---

# Email Sequence

## Overview

One sequence = one job (activate, educate, win back), decomposed into emails where each has a single goal and a reason to arrive on its day. Drafts and logic only — loading into the sending tool and pressing go is the user's move.

## When to Use

- Lifecycle sequences: post-signup onboarding, trial-to-paid, post-purchase, re-engagement, event follow-up
- NOT for: one-off broadcasts (just write the email), cold outreach at scale, or anything relying on deception — fake "Re:" subjects, false scarcity, misleading senders are refused regardless of conversion lore

## Process

1. **Fix the frame.** Product, audience segment, the ONE conversion goal of the sequence, entry trigger (signed up, purchased, went quiet), sending constraints (tool, plain-text vs. designed, sender identity), language and brand voice (ask for 1–2 example emails the user likes).
2. **Map the sequence** before writing a word. Table: email #, day offset, job of this email, CTA. Defaults that work: onboarding 4–6 emails over 14 days, first one instant; re-engagement 3 emails over 10 days. Every email must earn its slot — "email 4: more value" is not a job; cut it.
3. **Define exit and branch conditions:** conversion exits the sequence (nothing is dumber than "upgrade now" sent to someone who upgraded yesterday); hard bounce/unsubscribe exits everything; optional branch: did the key action vs. didn't.
4. **Draft each email:**
   - Subject ≤45 chars + one alternative variant; preheader that continues (not repeats) it
   - Body 50–125 words for action emails, up to 200 for educational ones; one CTA, stated once mid-email and once at the end max
   - Personalization slots as explicit tokens (`{first_name}`, `{trigger_feature}`) with a written fallback for each ("there" is not a fallback — restructure the sentence instead)
   - Day-1 email answers "what do I do right now"; every later email opens with value, not "just checking in"
5. **Compliance floor** (non-negotiable): honest sender name, working unsubscribe mention in every email, physical-address slot where the user's jurisdiction requires it (CAN-SPAM/GDPR-style rules), no purchased-list assumptions — sequence entry implies consent.
6. **Deliver** one Markdown file: sequence map table → per-email blocks (subject variants, preheader, body, tokens+fallbacks, exit checks) → implementation notes for the user's sending tool.

## Verification

- [ ] Every email has exactly one job and one CTA; none is "just more value"
- [ ] Exit-on-conversion defined — no post-conversion pitch emails possible
- [ ] Every personalization token has a real fallback
- [ ] No deceptive subjects, fake urgency, or consent-free assumptions anywhere

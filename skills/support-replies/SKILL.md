---
name: support-replies
description: Drafts customer support replies grounded strictly in a provided knowledge base (docs, FAQ, policies) — with citations per claim and explicit escalation when the KB has no answer. Use when asked to "answer this ticket", "draft support replies", "respond using our docs", "ответь клиенту по базе знаний", "разбери тикеты".
---

# Support Replies

## Overview

Ticket + knowledge base → reply draft where every factual claim cites its KB source, and questions the KB can't answer get escalated instead of improvised. Grounding is the whole point: a fluent wrong answer is worse than "let me check".

## When to Use

- Drafting replies to support tickets/emails/chat questions against docs, FAQ, help center, or policy files
- NOT for: inventing policy on the fly, account-specific actions (refunds, data changes — always escalate), or legal/medical judgment calls

## Process

1. **Load the knowledge base.** Docs folder, help-center URLs, FAQ file — whatever the user provides. If none: stop and ask; this skill does not run KB-less.
2. **Parse the ticket:** the actual question(s) — often more than one, customer's emotional state, product area, and any account-specific request.
3. **Find the answer in the KB** for each question. Note the exact source (file/section/URL). Three outcomes per question:
   - **Covered** — KB answers it → draft from the KB content
   - **Partial** — KB answers a nearby question → answer what's covered, mark the gap
   - **Not covered** — escalate; never bridge the gap with plausible-sounding product claims
4. **Draft the reply:** greet by name if known and mirror the customer's language; acknowledge frustration in one sentence when present (skip corporate apology theater); answer each question in asked order — concrete steps numbered; account-specific actions → "passing to the team" escalation phrasing; close with the single most likely follow-up preempted.
5. **Attach the grounding block** (for the user, stripped before sending): per claim — the KB source it came from; per escalation — what was missing from the KB.
6. **Batch mode:** multiple tickets → group by root cause first; identical root cause = one canonical draft adapted per customer, plus a note "N tickets, same cause" (that's a product signal, surface it).
7. **KB gap report:** after any run, list questions the KB couldn't answer — that's the docs backlog.

## Verification

- [ ] Every product/policy claim in drafts has a KB citation in the grounding block
- [ ] Zero claims sourced from general knowledge about "how products usually work"
- [ ] Escalations are explicit — no confident filler where the KB was silent
- [ ] Tone check: answers the human, not just the ticket

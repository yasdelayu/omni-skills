---
name: meeting-notes
description: Turns a meeting transcript or recording notes into a decision log, owned action items with deadlines, open questions, and a ready-to-send follow-up message. Use when asked to "summarize this meeting", "action items from the call", "make notes from transcript", "саммари встречи", "разбери созвон".
---

# Meeting Notes

## Overview

Transcript → the four things people actually reopen later: what was decided, who does what by when, what stayed unresolved, and the follow-up to send. Prevents the default failure — a prose retelling nobody reads.

## When to Use

- Any meeting artifact: transcript, auto-captions export, rough live notes
- NOT for: real-time meeting assistance, or transcribing audio (transcribe first with an available tool, then apply this skill)

## Process

1. **Identify the frame.** Meeting purpose, participants (map speaker labels to names if the user provides them), and date. Unknown speakers stay as "Speaker 2" — never guess identities.
2. **Extract decisions.** A decision = something the group settled ("we ship Friday", "we drop the feature"). Quote-anchor each: append the transcript phrase it comes from. Proposals that got no agreement are NOT decisions — they go to open questions.
3. **Extract action items.** Each needs owner + verb + deadline. Missing owner or deadline → mark `⚠ unassigned` / `⚠ no deadline` — surfacing gaps is half this skill's value. Vague intentions ("we should look into X sometime") get listed separately as "mentioned, not committed".
4. **Extract open questions and risks** — anything explicitly parked, disputed, or blocking.
5. **Write the summary** — 3–5 sentences max, decisions-first, no play-by-play.
6. **Draft the follow-up message** (email/chat, match the user's language): thanks-one-liner, decisions, action list by owner, open questions with who's expected to answer. Ready to paste — but the user sends it.
7. **Deliver** as one Markdown file: Summary / Decisions / Action items (table: owner, task, deadline, flags) / Open questions / Follow-up draft.

## Verification

- [ ] Every decision traces to a transcript quote; no proposal promoted to decision
- [ ] Every action item has owner and deadline or an explicit ⚠ flag
- [ ] Nothing in the output that isn't in the transcript — zero invented commitments
- [ ] Follow-up draft is standalone-readable for someone who missed the meeting

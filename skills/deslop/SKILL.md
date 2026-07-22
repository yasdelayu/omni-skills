---
name: deslop
description: Edits text to remove AI-writing tells and empty filler — cliché phrases, uniform rhythm, formulaic structure, unsourced statistics — while preserving meaning and the author's voice. Use when asked to "make this sound less AI", "remove the slop", "humanize this text", "убери ИИ-стиль", "звучит как нейросеть, перепиши".
---

# Deslop

## Overview

A slop pass is editing, not paraphrasing: cut what says nothing, ground what claims something, break the rhythm a generator defaults to. The output must say more per word, not just different words. This is editorial quality work — text passed through it reads better to humans; fooling detectors is not the goal and not a promise.

## When to Use

- Drafts (AI-assisted or not) that read generic, padded, or machine-flavored
- NOT for: academic dishonesty (ghost-writing graded work to hide authorship), or texts whose problem is substance — deslopping a content-free draft yields shorter content-free draft; say so and ask for facts instead

## Process

1. **Scan before touching.** Mark every hit against the three tell classes below. Report the count; if the text is clean, say so and stop — don't invent edits to justify the pass.
2. **Phrase tells** — delete or replace with a concrete statement. Core veto list (extend by language):
   - EN: "in today's fast-paced world", "delve into", "it's important to note", "plays a crucial role", "comprehensive approach", "landscape/realm/tapestry of", "unlock the potential", "game-changer", "at the end of the day", "in conclusion"
   - RU: «в современном мире», «давайте разберёмся», «стоит отметить», «играет ключевую роль», «комплексный подход», «на сегодняшний день», «не секрет, что», «подводя итог», «уникальная возможность», «в данной статье мы рассмотрим»
   - Any English buzzword transliterated awkwardly into a non-English text
3. **Structural tells** — rewrite the pattern, not just the words:
   - Three+ consecutive paragraphs of near-identical length and cadence → vary: merge two, cut one to a single line
   - Every H2 built on the same template ("What is X" / "Why X matters") → retitle to the section's actual claim
   - Lists where every item shares grammar but carries no distinct information → collapse to prose or cut items
   - Hedging stacks ("arguably one of the most...") → commit or delete
4. **Fact tells** — the credibility layer:
   - "Studies show / experts believe" without a named study or expert → name it (ask the user or check the source material) or delete the claim
   - Suspiciously round statistics with no source → same treatment
   - Generic examples ("a company might...") where the source material contains a real one → use the real one
5. **Preserve while cutting:** the author's actual voice quirks, technical precision, and all facts — deslop never changes meaning. If a cut would lose information, it's not slop; leave it.
6. **Deliver:** the edited text + a short change log (per tell class: count found → what was done) so the user sees this was surgery, not a rewrite.

## Verification

- [ ] Zero veto-list hits remain; structural rhythm varies (spot-check paragraph lengths)
- [ ] Every surviving statistic has a source; every deleted claim is in the change log
- [ ] Meaning preserved — diff review shows no factual drift
- [ ] Text got denser: word count dropped or information content rose, never the reverse

---
name: repurpose-content
description: Turns one piece of content (article, video transcript, idea, announcement) into platform-native posts for X/Twitter, LinkedIn, Telegram, Instagram, Threads, and Reddit. Use when asked to "repurpose this", "make posts from this article", "adapt for social media", "разбей на посты", "адаптируй под соцсети".
---

# Repurpose Content

## Overview

One source → a set of posts, each written natively for its platform. The failure mode this skill prevents: pasting the same text everywhere with different hashtags.

## When to Use

- An article, launch note, video transcript, or raw idea needs distribution across social platforms
- NOT for: writing the source article itself (that's a writing task), or posting/scheduling (agents draft; the user publishes)

## Process

1. **Extract the core.** Read the source and pull out: the single main claim, 3–5 supporting facts or numbers, one contrarian or surprising angle, and any quotable line. If the source has none of these, say so — thin sources make thin posts.
2. **Ask which platforms** if not specified. Default set: X, LinkedIn, Telegram.
3. **Write each post from the extracted core, not from the previous post.** Platform rules:
   - **X/Twitter** — single post ≤280 chars, or thread of 5–7 tweets. First tweet must work standalone. No hashtags unless the user's niche uses them. Line breaks over commas.
   - **LinkedIn** — 900–1300 chars. First 2 lines carry the hook (that's all that shows before "…see more"). Short paragraphs, one idea each. End with a question or a take, not "Thoughts?".
   - **Telegram** — 400–800 chars, denser and more direct than LinkedIn. Bold the key phrase. One link max, at the end.
   - **Instagram** — caption ≤2200 chars, hook in first 125 (grid cutoff). Suggest a visual concept (what the image/carousel shows). 3–5 niche hashtags, not 30.
   - **Threads** — ≤500 chars, conversational, one thought. No corporate tone.
   - **Reddit** — value-first post for a named subreddit; zero self-promotion in the body, source link only if subreddit rules allow. Match the subreddit's register.
4. **Vary the angle.** At least two posts must lead with different facts or framings from the extraction — not the same opening idea restyled.
5. **Deliver** as one Markdown file with a section per platform, each post ready to copy-paste.

## Verification

- [ ] Every post works standalone without reading the source
- [ ] No two posts share an opening line or identical structure
- [ ] Character limits respected (count the longest post)
- [ ] Hooks are in the first line/125 chars where the platform truncates
- [ ] Nothing invented: every fact in the posts traces to the source

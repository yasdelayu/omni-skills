---
name: new-skill
description: Scaffolds a new skill in this repository following the house format — frontmatter contract, section layout, and catalog registration. Use when adding a skill to omni-skills, or when the user says "add a skill", "create a skill for X", "новый скилл", "сделай скилл".
---

# New Skill

## Overview

Creates a new skill directory with a spec-compliant `SKILL.md` and registers it in the repository catalog. Ensures every skill in this repo stays discoverable and portable across agents.

## Process

1. **Name it.** Lowercase, hyphen-separated, verb-first when it's an action (`review-landing`, `write-tg-post`). Check `skills/` for an existing skill that already covers the need — extend it instead of duplicating.
2. **Create `skills/<name>/SKILL.md`** from the template below. The directory name must equal frontmatter `name`.
3. **Write the description last**, after the body is done. It must state *what* the skill does (third person) and *when* to trigger it ("Use when …" with concrete phrases a user would actually type). No workflow steps in the description.
4. **Keep it lean.** Body under ~150 lines. Reference material over ~100 lines → `references/*.md` inside the skill dir. Runnable helpers → `scripts/`. Create neither unless actually needed.
5. **Register it.** Add a row to the catalog table in `README.md`.

## Template

```markdown
---
name: skill-name
description: [What it does, third person]. Use when [trigger phrases the user would type].
---

# Skill Title

## Overview
One-two sentences: what this skill does and why it matters.

## When to Use
- Positive triggers
- NOT for: exclusions

## Process
1. Concrete, actionable steps — commands, not vibes.
2. "Run `npm test` and verify all pass", not "make sure tests work".

## Verification
- [ ] Exit criteria checkable with evidence (test output, screenshot, diff)
```

Drop sections that don't apply; add `## Common Rationalizations` (excuse → rebuttal table) for skills agents tend to shortcut.

## Verification

- [ ] Directory name equals frontmatter `name`
- [ ] Description has both *what* and "Use when" triggers, ≤1024 chars
- [ ] No links pointing outside the skill's directory
- [ ] Row added to the catalog table in `README.md`

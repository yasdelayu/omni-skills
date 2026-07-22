# AGENTS.md

Guidance for AI coding agents (Claude Code, Cursor, Codex, Copilot, etc.) working in this repository.

## Project overview

Omni Skills is a collection of universal Agent Skills following the [Agent Skills specification](https://agentskills.io/specification). Skills live in `skills/<name>/SKILL.md` and are agent-agnostic: no agent-specific syntax in skill bodies.

## House rules for skills

- Frontmatter: `name` (lowercase-hyphenated, must match the directory name) and `description` (what it does in third person + one or more "Use when" triggers, max 1024 chars). Optional: `license`, `metadata`.
- The description is what agents see when deciding to activate the skill — put triggers there, not workflow steps.
- Keep `SKILL.md` under ~150 lines. Reference material over ~100 lines goes to `references/` inside the skill directory; runnable helpers go to `scripts/`. No empty directories.
- Skills must be self-contained: never link to files outside the skill's own directory.
- Write skills in English. Trigger phrases may include other languages when useful.
- When adding a skill, follow `skills/new-skill/SKILL.md` and update the catalog table in `README.md`.

## Directory structure

```
skills/
  <skill-name>/
    SKILL.md           # Required
    references/        # Optional, loaded on demand
    scripts/           # Optional, runnable helpers
```

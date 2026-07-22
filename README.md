# Omni Skills

Universal [Agent Skills](https://agentskills.io/) that work with any AI coding agent — Claude Code, Cursor, Codex, OpenCode, Gemini CLI, Copilot, and anything else that reads Markdown.

One format. Every agent. Each skill is a folder in `skills/` with a `SKILL.md` inside: YAML frontmatter (`name` + `description` with "Use when" triggers) followed by the workflow. Agents discover skills by description and load the body on demand.

## Available skills

| Skill | Description | Use when |
|-------|-------------|----------|
| **[new-skill](skills/new-skill/SKILL.md)** | Scaffold a new skill in this repository following the house format | "Add a skill", "create a skill for X", "новый скилл" |

More coming — this catalog grows as skills are added.

## Installation

### Any agent (recommended)

```bash
npx skills add yasdelayu/omni-skills
```

Installs into Claude Code, Cursor, Codex, OpenCode, and others automatically.

### Claude Code (plugin)

```text
/plugin marketplace add yasdelayu/omni-skills
/plugin install omni-skills@omni
```

Skills become namespaced (`/omni-skills:new-skill`) and update with `/plugin update`.

### Manual

```bash
cp -r skills/* ~/.claude/skills/
```

Or paste a `SKILL.md` into project knowledge / the conversation for web-based agents.

## Usage

Skills activate automatically when your request matches their description — no explicit invocation needed. Agents that support slash commands can also invoke them directly by name.

## Adding a skill

Ask your agent to "add a skill for X" — the [new-skill](skills/new-skill/SKILL.md) skill walks it through the house format. Or copy the template from that file by hand.

Structure:

```
omni-skills/
├── README.md            # This file — keep the catalog table in sync
├── AGENTS.md            # Guidance for agents working in this repo
├── LICENSE              # MIT
├── .claude-plugin/      # Claude Code plugin + marketplace manifests
└── skills/
    └── <skill-name>/
        ├── SKILL.md     # Required — frontmatter + workflow
        ├── references/  # Optional — docs loaded on demand
        └── scripts/     # Optional — runnable helpers
```

## License

MIT

# Omni Skills

Universal [Agent Skills](https://agentskills.io/) that work with any AI coding agent — Claude Code, Cursor, Codex, OpenCode, Gemini CLI, Copilot, and anything else that reads Markdown.

One format. Every agent. Each skill is a folder in `skills/` with a `SKILL.md` inside: YAML frontmatter (`name` + `description` with "Use when" triggers) followed by the workflow. Agents discover skills by description and load the body on demand.

## Available skills

| Skill | Description | Use when |
|-------|-------------|----------|
| **[repurpose-content](skills/repurpose-content/SKILL.md)** | One article/idea → platform-native posts for X, LinkedIn, Telegram, Instagram, Threads, Reddit | "Repurpose this", "make posts from this article", "адаптируй под соцсети" |
| **[competitor-watch](skills/competitor-watch/SKILL.md)** | Snapshot-and-diff monitoring of competitor pricing/features pages, change-only reports | "Check competitors", "monitor pricing", "что изменилось у конкурентов" |
| **[lead-scout](skills/lead-scout/SKILL.md)** | ICP → verified prospect list from public sources + personalized outreach drafts (never sends) | "Find leads", "build a prospect list", "найди лидов" |
| **[seo-article](skills/seo-article/SKILL.md)** | Keyword → SERP recon, gap-driven outline, draft, on-page SEO pass with title/meta/schema | "Write an SEO article", "rank for X", "статья под ключевик" |
| **[news-digest](skills/news-digest/SKILL.md)** | Deduplicated, cited news digest on a topic for a period, ranked by impact | "News digest", "what happened in X this week", "дайджест новостей" |
| **[review-sentiment](skills/review-sentiment/SKILL.md)** | Reviews across platforms → sentiment split, quoted themes, action-ranked report | "Analyze reviews", "what do customers say about X", "анализ отзывов" |
| **[new-skill](skills/new-skill/SKILL.md)** | Scaffold a new skill in this repository following the house format | "Add a skill", "create a skill for X", "новый скилл" |

The first six are adapted from the most-visited automation patterns on [n8nworkflows.xyz](https://n8nworkflows.xyz/) (10k+ workflow catalog), rebuilt as agent-native instruction workflows — no n8n required.

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

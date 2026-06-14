# claude-prompt-tools

A small collection of [Claude Skills](https://support.claude.com/en/articles/12512180-use-skills-in-claude) for getting dramatically better results from any LLM.

Starting with **prompt-enhancer**: hand it a rough, vague, or half-formed prompt, and it rewrites it into a fully structured, expert-grade prompt — role, context, deliverable, success criteria, anti-hallucination guards, the works. Mediocre prompt in, expert prompt out.

---

## What's inside

| Skill | What it does |
|-------|--------------|
| `prompt-enhancer` | Rewrites any rough prompt into a comprehensive, high-quality version that gets dramatically better results from any LLM (ChatGPT, Claude, Gemini, Copilot, Midjourney, etc.). |

---

## Install

There are two ways to use this, depending on where you run Claude.

### Option A — Claude Code (recommended, auto-updates)

Add this repo as a plugin marketplace once, then install the plugin:

```bash
claude plugin marketplace add YOUR_GITHUB_USERNAME/claude-prompt-tools
claude plugin install prompt-enhancer@claude-prompt-tools
```

When the skill is updated here, you get the new version on your next pull. To update:

```bash
claude plugin marketplace update claude-prompt-tools
```

### Option B — Claude.ai / Cowork (manual upload)

1. Download or clone this repo.
2. Zip the skill folder: `plugins/prompt-enhancer/skills/prompt-enhancer/` (the folder containing `SKILL.md`).
3. In Claude, go to **Settings → Capabilities → Skills** (or **Customize → Skills**) and upload the `.zip`.
4. Toggle it on. Uploaded skills are private to your account.

> The exact menu path can shift between releases — if you don't see it, check the current flow in the [Claude Skills help article](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

---

## How to use it

Once installed, just talk to Claude naturally. The skill fires on its own when you ask things like:

- "Improve this prompt: ..."
- "Make this prompt better — it's not working."
- "Help me prompt for [task]."
- "Turn this into a proper prompt: ..."

You'll get back a clean, copy-paste-ready prompt plus a short **What Changed** diff explaining the improvements.

---

## Repo structure

```
claude-prompt-tools/
├── .claude-plugin/
│   └── marketplace.json          # marketplace manifest (lists the plugins)
├── plugins/
│   └── prompt-enhancer/
│       ├── .claude-plugin/
│       │   └── plugin.json        # plugin metadata
│       └── skills/
│           └── prompt-enhancer/
│               └── SKILL.md       # the actual skill
└── README.md
```

---

## Contributing

Found a way to make the enhancer sharper? Open an issue or a PR. Feedback on what's missing is genuinely welcome — that's the point.

## License

MIT — use it, fork it, build on it.

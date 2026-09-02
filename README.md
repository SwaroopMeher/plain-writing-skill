# Plain Writing Skill

A writing style skill for AI assistants. It makes the model write plain, human English instead of AI slop.

The whole skill is one file, [SKILL.md](SKILL.md). It works with Claude, Codex, Gemini, Cursor, and any assistant that accepts custom instructions.

![License](https://img.shields.io/badge/license-MIT-green)

## What it does

- Short sentences, one idea per sentence, common words.
- Bans AI tics. "delve", "robust", "It's not X, it's Y", "Great question!", fake drama, hype adjectives, colon reveals, fake-profound endings.
- Bans sycophancy. The model acts on your point instead of complimenting it.
- Keeps full information. Plain means clear, not incomplete. Rewrites keep every fact and example.

Before and after:

> Bad: "Great question! Let's unpack this. At the end of the day, the crucial insight is that caching isn't about speed, it's about cost."
>
> Good: "Caching here saves cost. The requests were already fast, so there was no time to save."

## Install

### Claude Code

```bash
git clone https://github.com/SwaroopMeher/plain-writing-skill.git
mkdir -p ~/.claude/skills/plain-writing
cp plain-writing-skill/SKILL.md ~/.claude/skills/plain-writing/SKILL.md
```

Claude Code picks it up automatically. You can also invoke it with `/plain-writing`.

For one project only, copy it to `.claude/skills/plain-writing/SKILL.md` inside the project instead.

### Claude.ai

Paste the body of `SKILL.md` (everything below the frontmatter) into a Project's custom instructions, or into Settings > Profile > personal preferences.

### OpenAI Codex

Paste the body of `SKILL.md` into `AGENTS.md` in your repo, or into `~/.codex/AGENTS.md` for all projects.

### Gemini CLI

Paste the body of `SKILL.md` into `GEMINI.md` in your repo, or into `~/.gemini/GEMINI.md` for all projects.

### Cursor

Paste the body of `SKILL.md` into a rule under `.cursor/rules/`, or into Settings > Rules for AI.

### Anything else

Paste the body of `SKILL.md` into the system prompt or custom instructions. The file is plain markdown with no tool calls, so it works anywhere.

## Customize

The skill is generic on purpose. Two things you may want to add for yourself.

1. What you already know. Add a short section like "The user knows Python and SQL. Do not re-explain those." The model will then skip basics you do not need.
2. Your own banned words. Add them to the lists in `SKILL.md`.

## License

MIT. See [LICENSE](LICENSE).

## Author

**Swaroop Meher** - [@SwaroopMeher](https://github.com/SwaroopMeher)

# Founder's Playbook Skill

An executable AI agent skill encoding Anthropic's **36-page Founder's Playbook** — the 4-phase framework for building AI-native startups.

## What It Does

This skill turns Anthropic's founder manual into **enforceable agent rules**. Any AI agent (Claude Code, Hermes, Cursor, Codex) that loads this skill will:

- Detect which phase your project is in (IDEA → MVP → LAUNCH → SCALE)
- Enforce phase-gated discipline (don't build before validation)
- Prevent "Agentic Technical Debt" by requiring CLAUDE.md before code
- Run Devil's Advocate exercises on new ideas
- Apply the Sean Ellis PMF test before claiming product-market fit
- Build AI-proof moats (domain expertise, workflow lock-in, user data)

## The Four Phases

| Phase | Question | Rule |
|-------|----------|------|
| **IDEA** | Is this worth doing? | Validate before you build. Play Devil's Advocate. |
| **MVP** | What should we build first? | CLAUDE.md first, code second. Prevent agentic technical debt. |
| **LAUNCH** | Can this grow? | Repay tech debt. Don't be the bottleneck. |
| **SCALE** | Is this sustainable? | Build three moats AI can't copy. |

## Installation

### Claude Code
```bash
# Copy to your skills directory
cp -r founder-playbook ~/.claude/skills/
```

### Hermes Agent
```bash
# Hermes auto-discovers skills in ~/.hermes/skills/
cp -r founder-playbook ~/.hermes/skills/startup/
```

### Cursor / Codex / Other Agents
This skill uses the [agentskills.io](https://agentskills.io) SKILL.md format — compatible with any agent that supports the standard.

## Core Principles

1. **Execution is no longer scarce. Judgment is.** Your role shifts from "individual contributor" to "AI agent orchestrator."
2. **CLAUDE.md is the antidote to Agentic Technical Debt.** Without persistent architecture docs, AI sessions drift independently.
3. **42% of startups fail by building things nobody wanted.** AI makes this risk HIGHER, not lower, by compressing build time.
4. **PMF is not launch hype.** Run the Sean Ellis test: >40% "very disappointed" users.

## Author

**Chen Hui** ([@chenhuiai](https://github.com/chenhuiai)) — adapted from Anthropic's original playbook with Claude Code.

## Source

Based on [The Founder's Playbook](https://claude.com/blog/the-founders-playbook) by Anthropic (May 14, 2026).

## License

CC-BY-4.0 — same as the original Anthropic content.

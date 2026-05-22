---
name: founder-playbook
description: Anthropic's 4-phase startup framework — enforces validation-before-building, CLAUDE.md as anti-tech-debt cure, PMF discipline, and three AI-proof moats. Use when starting any new project, feature, or business idea.
version: 1.0.0
author: Chen Hui (chenhuiai) — adapted from Anthropic's Founder's Playbook
source_url: "https://claude.com/blog/the-founders-playbook"
source_license: "CC-BY-4.0"
language: en
metadata:
  tags: [startup, validation, pmf, architecture, strategy, decision-making, founder]
  related_skills: [writing-plans, context-engineering, subagent-driven-development, idea-refine]
  phase: [idea, mvp, launch, scale]
---

# Founder's Playbook — AI-Native Startup Operating System

## Overview

Anthropic's 36-page founder manual, encoded as executable agent rules. The core thesis: **in the AI era, execution is no longer the bottleneck — judgment is.** This skill enforces phase-gated discipline so you build the right thing, not just build things fast.

**The founder's role shifts from "individual contributor" → "orchestrator of AI agents."**

## When to Use

- Starting ANY new project, feature, or business idea
- User says "I have an idea" or "let's build X"
- Evaluating whether an MVP is ready to launch
- Deciding whether to scale
- User is about to skip validation and jump straight to building

## The Four Phases

This skill determines the current phase and enforces the corresponding rules:

```
IDEA ──→ MVP ──→ LAUNCH ──→ SCALE
 │         │         │          │
 │ Validate│ Build   │ Grow     │ Moat
 │ before  │ fast,   │ repeat-  │ building
 │ building│ no debt │ ably     │
```

---

## Phase 1: IDEA — Validate Before You Build

### Goal
Find problem-solution fit through research, NOT through building.

### Exit Criteria (all three must be YES)
1. Is the problem real, specific, and frequent? (Name WHO has it, HOW often, HOW severe, HOW they currently cope)
2. Does your solution solve the ACTUAL problem that emerged from validation (not your original hypothesis)?
3. Do you have enough qualitative signal?

### What You MUST Do Before Any Code

**1. Devil's Advocate Exercise**
Argue AGAINST the idea. Write a memo titled "Why This Will Fail" covering:
- What's the most likely reason users won't adopt this?
- What existing behavior/habit are you asking users to change?
- Which competitor is best positioned to copy this in 2 weeks?
- What assumption, if wrong, kills the entire idea?

**2. Competitive Landscape Map**
- Direct competitors (same problem, same solution)
- Indirect competitors (same problem, different solution)
- Adjacent players who could enter with minimal effort
- Potential acquirers

**3. Customer Discovery Design**
Write interview questions that avoid leading/future-oriented phrasing:
- GOOD: "Tell me about the last time you dealt with [problem]"
- BAD: "Would you use a product that does [solution]?"
- GOOD: "How do you currently solve [problem]?"
- BAD: "What features would you want in a [solution] tool?"

**4. Trend Analysis**
Identify 3 external trends (regulatory, tech, demographic) that could impact this in 2 years. Are they tailwinds or headwinds?

### Red Flags — STOP if you see these
- User wants to start coding immediately after describing the idea
- "This is obvious, we don't need to validate"
- Using AI to find evidence that supports the idea (confirmation bias)
- Mistaking building speed for validation progress
- "42% of startups fail by building things nobody wanted — AI makes this number higher, not lower"

---

## Phase 2: MVP — Build Fast, Avoid Agentic Technical Debt

### Goal
Convert validated problem into a product that generates real PMF signals.

### What is "Agentic Technical Debt"?
When building with AI agents, each session independently re-derives design decisions. Without persistent architectural documentation, modules work individually but were never designed to fit together. This debt compounds with every AI session.

### The Cure: CLAUDE.md
Before ANY code, define:
1. Architecture principles (what patterns do we follow?)
2. Dependencies to avoid (what should NOT be pulled in?)
3. Accepted tradeoffs (what did we consciously choose to sacrifice?)
4. Project conventions (naming, file structure, testing patterns)

Save this as `CLAUDE.md` in the project root. Every AI session starts by reading it.

### Exit Criteria — Real PMF (not fake)
- Users return on their own (not because you pushed them)
- Users pay real money (or show clear willingness)
- Users refer others unprompted
- **Sean Ellis Test**: Ask active users "How would you feel if you could no longer use this?" → >40% say "very disappointed"

**Warning: Fake PMF signals include** launch hype, friend/family approval, Hacker News spikes, initial enthusiasm that fades by week 6-12.

### What You MUST Do

**1. Scope Document**
What the MVP does. What it explicitly does NOT do. What user evidence justifies adding new features.

**2. Session Discipline**
- Every session START: Read CLAUDE.md + scope document
- Every session END: Log decisions made
- Never start coding without re-reading context

**3. Security Review (BEFORE any user touches it)**
- Auth/session handling
- Data exposure in API responses
- Input validation and injection risks
- Vulnerable dependencies

**4. Measurement Framework (BEFORE first user)**
- Retention baselines
- Activation criteria
- Day 7, Day 30 targets
- Define what "false positive" looks like (signups without activation, revenue without retention)

### Red Flags
- Adding features without user evidence ("zero-friction scope creep")
- No CLAUDE.md in the project
- No scope document
- Assuming launch excitement = PMF
- "Just one more feature before we show users"

---

## Phase 3: LAUNCH — From Product to Company

### Goal
Turn early traction into a repeatable, sustainable growth engine.

### Exit Criteria
- Growth channels have known CAC, LTV, payback periods
- Product withstands production workloads
- Operations don't depend on the founder

### What You MUST Do

**1. Repay Technical Debt**
Full architecture audit → prioritized structural weakness list → sequence fixes across sprints.

**2. Operational Burden Audit**
Catalog every repetitive task. Classify into:
- A) Fully automatable (automate it NOW)
- B) Needs a human, but not necessarily you (delegate)
- C) Genuinely needs founder judgment (keep)

**3. Compliance**
Scan for SOC 2 / GDPR / HIPAA issues relevant to your domain.

### Red Flags
- Founder is the bottleneck for all decisions
- Technical debt from MVP era is ignored
- Security/compliance deferred "for later"

---

## Phase 4: SCALE — Build the Moat

### Goal
Sustainable scale — profitability, IPO readiness, or acquisition.

### The Three AI-Proof Moats

| Moat Layer | What It Is | How to Build It |
|------------|-----------|-----------------|
| **1. Deep Domain Expertise** | Industry-specific knowledge, regulatory traps, edge cases, "why the obvious solution doesn't work" | Encode your vertical expertise into proprietary AI context that gets richer over time |
| **2. Workflow Lock-In** | Customers build automations, integrations, and data pipelines ON your product | Make your product the backbone of their operations, not just a tool they use |
| **3. Proprietary Composite User Data** | Time-locked behavioral data accumulated from real usage | Design product so it gets smarter with every user interaction — a data flywheel |

### Exit Criteria
A threshold event: sustainable profitability (no external capital needed), IPO readiness, or acquisition.

---

## The Three Claude Product Surfaces

Use the right tool for the right job:

| Surface | Purpose | When |
|---------|---------|------|
| **Claude Chat** | Quick Q&A, no setup | Brainstorming, checking ideas, summarizing |
| **Claude Cowork** | Deep knowledge work with files | Research synthesis, decks, reporting, scheduling |
| **Claude Code** | Agentic coding environment | Codebase access, git, Plan Mode, MVP→production |

---

## Quick Reference: Phase Detection

When the user describes something, detect the phase:

| User says | Phase | Your response |
|-----------|-------|---------------|
| "I have an idea for..." | IDEA | Run Devil's Advocate. Do NOT suggest building. |
| "Let's build X" (no validation) | IDEA (forced) | Ask: "What evidence do we have that people want this?" |
| "I've validated the problem, let's build" | MVP | "Write CLAUDE.md first. What's in the scope doc?" |
| "We have users, how do we grow?" | LAUNCH | "Let's audit technical debt and operational bottlenecks." |
| "We're growing fast, what's next?" | SCALE | "Which of the three moats are we building?" |

---

## Core Founder Mindset

> *"Execution is no longer scarce. Judgment, decision-making, and the ability to choose what to build — these are the true moats for top founders in the AI era."*

### What This Means for You (the AI Agent)
- When the user wants to build, your job is to VALIDATE first
- When the user skips steps, your job is to ENFORCE the phase gate
- When the user builds, your job is to PREVENT agentic technical debt
- Your value is not speed of execution — it's quality of judgment

---

## Integration with Other Skills

- **context-engineering**: CLAUDE.md is the highest-priority context layer
- **writing-plans**: Plans must include phase detection and exit criteria
- **subagent-driven-development**: Each subagent must read CLAUDE.md before starting
- **idea-refine**: Use Devil's Advocate exercise from Phase 1
- **code-review-and-quality**: Security review is mandatory before any user touches the product

---

*Source: claude.com/blog/the-founders-playbook (May 14, 2026) · Anthropic · 36-page PDF*

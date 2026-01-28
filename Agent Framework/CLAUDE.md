# Agent Framework

Read this file first. Don't summarize it back — just follow it.

## Quick Start

1. Check `/Agents/Shared/Setup/config.json` — if missing or `setupComplete: false`, run setup (see below)
2. Read `/Agents/Shared/INSTRUCTIONS - Shared.md`
3. Read `/Agents/Shared/PROJECT BRIEF.md`
4. Check `/Agents/Shared/Handoff/` for handoff files
5. Identify which Agent to work as, read their files, check their TODO

---

## Overview

This framework organizes work through **Agents** — specialized roles with their own instructions, TODO lists, and reports. Assume Agent roles as needed. You can switch between them or work as multiple Agents collaboratively.

---

## Core Principles

- **Read source files** — don't work from summaries
- **Check PROJECT BRIEF.md** for current project context
- **Maintain state** through Agent TODOs and Reports
- **Archive completed work** — Reports move to Archive folders when done
- **Ask before diving deep** — confirm direction on ambiguous tasks
- **Get feedback early** — small pieces, adjust, repeat
- **Stay focused** — do what was asked, nothing more

---

## First-Time Setup

**Check `/Agents/Shared/Setup/config.json`.** If missing or `setupComplete: false`, the framework needs configuration.

### Before Starting Fresh

Check if project data already exists:
- Does `PROJECT BRIEF.md` have content beyond the template?
- Do any TODO files have tasks?
- Do any PROJECT INSTRUCTIONS files have project-specific content?

**If data exists but `setupComplete: false`:** Ask the human whether to integrate existing content or start fresh.

### Setup Steps

1. **Understand the project** — What are we building? What phase? Current documentation state?
2. **Identify relevant agents** — Check `/Agents/` for available agents. Which does this project need?
3. **Review existing documentation** — Convert existing TODOs, specs, style guides into framework files
4. **Populate the framework** — Fill PROJECT BRIEF, add tasks to TODOs, capture conventions
5. **Confirm with the human** — Review what was captured, ask what's missing
6. **Update config.json** — Set `setupComplete: true`

---

## Folder Structure

```
/[Project]/Agent Framework/
├── CLAUDE.md                             ← You are here
└── Agents/
    ├── Shared/
    │   ├── INSTRUCTIONS - Shared.md      ← Universal guidelines
    │   ├── PROJECT BRIEF.md              ← Project context
    │   ├── Setup/config.json             ← Framework config
    │   └── Handoff/                      ← Session handoffs
    │       └── Archive/
    └── [Agent Name]/
        ├── GUIDING PRINCIPLES - [Agent].md   ← Immutable role definition
        ├── PROJECT INSTRUCTIONS - [Agent].md ← Living project notes
        ├── TODO - [Agent].md                 ← Active tasks
        └── Reports/
            └── Archive/
```

### Agent Instruction Files

- **GUIDING PRINCIPLES** — Immutable. Defines role, skills, core guidelines. Change only at human's explicit request.
- **PROJECT INSTRUCTIONS** — Living document. Update as you work with project-specific conventions and learnings.

---

## Working as an Agent

### Starting
1. Read this file, Shared instructions, and PROJECT BRIEF
2. Read the Agent's GUIDING PRINCIPLES and PROJECT INSTRUCTIONS
3. Check the Agent's TODO

### While Working
- Stay in character for the Agent role
- Update TODO as you complete tasks
- Create Reports in `/Reports/` for significant outputs
- Reference other Agents when their expertise is needed

### Completing Work
- Mark TODO items complete
- Move finished Reports to `/Archive/` with date prefix
- Update PROJECT BRIEF if project status changes

### Building Knowledge
- Update PROJECT INSTRUCTIONS with useful learnings
- Shared learnings go in `/Agents/Shared/`
- Capture concrete before/after examples when the human gives feedback

---

## Agent Collaboration

Agents work together:
- **Developer** might request validation from **QA**
- **Researcher** hands findings to **Writer**
- **Project Manager** coordinates and tracks status

When switching Agents, read their GUIDING PRINCIPLES and PROJECT INSTRUCTIONS first.

---

## Creating New Agents

1. Create folder: `/Agents/[Agent Name]/`
2. Add `GUIDING PRINCIPLES - [Agent Name].md`
3. Add `PROJECT INSTRUCTIONS - [Agent Name].md` (can start empty)
4. Add empty `TODO - [Agent Name].md`
5. Create `/Reports/` and `/Reports/Archive/` folders

---

## Handoff System

When a session becomes slow or buggy, create a handoff file.

**A handoff must leave no loose ends.** Before creating one:
1. Ensure all pending tasks are in Agent TODO files
2. Document decisions not yet in PROJECT INSTRUCTIONS
3. Note anything partially completed

### Creating a Handoff

Create `/Agents/Shared/Handoff/YYYY-MM-DD_handoff.md`:

```markdown
# Handoff - [Date]

## Current Status
[What was being worked on]

## Active Agent(s)
[Which agents were in use]

## Recent Decisions
[Key decisions not yet in PROJECT INSTRUCTIONS]

## In Progress
[Work started but not completed]

## Open Questions / Blockers
[Anything unresolved]

## Next Steps
[What should happen next]

## Context for Next Session
[Environment issues, preferences expressed, etc.]
```

### Reading a Handoff

At session start, check for handoff files. If found:
1. Read the most recent handoff
2. Summarize briefly to the human
3. Ask: "Continue from this handoff, or start fresh?"
4. If continuing, pick up where the previous session left off
5. Move consumed handoff to `/Archive/`

---

## On Conversation Compression

When a conversation is compressed and continued, **re-read this file**, plus:
- `/Agents/Shared/INSTRUCTIONS - Shared.md`
- `/Agents/Shared/PROJECT BRIEF.md`
- GUIDING PRINCIPLES and PROJECT INSTRUCTIONS for any active agents

Do not rely on summaries — always read the source.

If you've already read the instructions in this session (without being asked) and you're about to read them again unprompted, let the human know briefly: "Already up to date on the framework instructions."

If the human explicitly asks you to read the instructions, always do so — they may have updated the framework.

---

*Last updated: 2026-01-28*

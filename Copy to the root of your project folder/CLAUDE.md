# Agent Framework

Read this file first. Don't summarize it back — just follow it.

## Quick Start

1. Check if `/Agent Data/` exists at the project root
   - **If missing:** This is a fresh install. Copy `Agent Data` from inside `Agent Framework` to the project root, then run setup (see below)
   - **If present:** Framework is installed. Continue to step 2
2. Read `/Agent Framework/INSTRUCTIONS - Shared.md`
3. Read `/Agent Data/PROJECT BRIEF.md`
4. Check `/Agent Data/Handoff/` for handoff files
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

**Check if `/Agent Data/` exists at the project root.** If missing, the framework needs installation.

### Installation

1. Copy the `Agent Data` folder from inside `Agent Framework` to the project root
2. Your structure should now be:
   ```
   /[Project]/
   ├── CLAUDE.md
   ├── Agent Framework/
   └── Agent Data/        ← Copied here
   ```

### Setup Steps

Once Agent Data is in place:

1. **Understand the project** — What are we building? What phase? Current documentation state?
2. **Identify relevant agents** — Check `/Agent Framework/Agents/` for available agents. Which does this project need?
3. **Review existing documentation** — Convert existing TODOs, specs, style guides into framework files
4. **Populate the framework** — Fill PROJECT BRIEF, add tasks to TODOs, capture conventions
5. **Confirm with the human** — Review what was captured, ask what's missing

---

## Folder Structure

```
/[Project]/
├── CLAUDE.md                               ← You are here
│
├── Agent Framework/                        ← FRAMEWORK FILES (replace on update)
│   ├── INSTRUCTIONS - Shared.md            ← Universal guidelines
│   ├── Agents/
│   │   └── [Agent Name]/
│   │       └── GUIDING PRINCIPLES - [Agent].md
│   └── Agent Data/                         ← Template (ignore if /Agent Data/ exists at root)
│
└── Agent Data/                             ← USER DATA (preserved on update)
    ├── PROJECT BRIEF.md                    ← Project context
    ├── Handoff/
    │   └── Archive/
    └── Agents/
        └── [Agent Name]/
            ├── PROJECT INSTRUCTIONS - [Agent].md ← Living project notes
            ├── TODO - [Agent].md                 ← Active tasks
            └── Reports/
                └── Archive/
```

### Where to Find Agent Files

- **GUIDING PRINCIPLES** → `/Agent Framework/Agents/[Agent]/` — Immutable role definition
- **PROJECT INSTRUCTIONS** → `/Agent Data/Agents/[Agent]/` — Living project notes
- **TODO** → `/Agent Data/Agents/[Agent]/` — Active tasks

### Updating the Framework

To update to a new version:
1. Delete the `/Agent Framework/` folder
2. Copy in the new `/Agent Framework/` folder
3. Done — your `/Agent Data/` is untouched

The `Agent Data` template inside `Agent Framework` is ignored when `/Agent Data/` already exists at root.

---

## Working as an Agent

### Starting
1. Read this file, then `/Agent Framework/INSTRUCTIONS - Shared.md`, then `/Agent Data/PROJECT BRIEF.md`
2. Read the Agent's GUIDING PRINCIPLES from `/Agent Framework/Agents/[Agent]/`
3. Read the Agent's PROJECT INSTRUCTIONS and TODO from `/Agent Data/Agents/[Agent]/`

### While Working
- Stay in character for the Agent role
- Update TODO as you complete tasks
- Create Reports in `/Agent Data/Agents/[Agent]/Reports/` for significant outputs
- Reference other Agents when their expertise is needed

### Completing Work
- Mark TODO items complete
- Move finished Reports to `/Archive/` with date prefix
- Update PROJECT BRIEF if project status changes

### Building Knowledge
- Update PROJECT INSTRUCTIONS with useful learnings
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

1. Create folder in both locations:
   - `/Agent Framework/Agents/[Agent Name]/`
   - `/Agent Data/Agents/[Agent Name]/`
2. Add `GUIDING PRINCIPLES - [Agent Name].md` to Agent Framework
3. Add `PROJECT INSTRUCTIONS - [Agent Name].md` to Agent Data (can start empty)
4. Add empty `TODO - [Agent Name].md` to Agent Data
5. Create `/Reports/` and `/Reports/Archive/` folders in Agent Data

---

## Handoff System

When a session becomes slow or buggy, create a handoff file.

**A handoff must leave no loose ends.** Before creating one:
1. Ensure all pending tasks are in Agent TODO files
2. Document decisions not yet in PROJECT INSTRUCTIONS
3. Note anything partially completed

### Creating a Handoff

Create `/Agent Data/Handoff/YYYY-MM-DD_handoff.md`:

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
- `/Agent Framework/INSTRUCTIONS - Shared.md`
- `/Agent Data/PROJECT BRIEF.md`
- GUIDING PRINCIPLES and PROJECT INSTRUCTIONS for any active agents

Do not rely on summaries — always read the source.

If you've already read the instructions in this session (without being asked) and you're about to read them again unprompted, let the human know briefly: "Already up to date on the framework instructions."

If the human explicitly asks you to read the instructions, always do so — they may have updated the framework.

---

*Last updated: 2026-01-28*

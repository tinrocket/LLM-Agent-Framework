# Agent Framework — Setup

Read this when `/Agent Data/` doesn't exist at the project root. For ongoing work, see `CLAUDE.md`.

---

## Installation

Create the Agent Data structure (don't copy the whole template — only what's needed):

1. Create `/Agent Data/` folder at project root
2. Copy `PROJECT BRIEF.md` from `/Agent Framework/Agent Data/`
3. Copy the `Handoff/` folder from `/Agent Framework/Agent Data/`
4. Create an empty `Agents/` folder inside `/Agent Data/`

Your structure should now be:
```
/[Project]/
├── CLAUDE.md
├── Agent Framework/
└── Agent Data/
    ├── PROJECT BRIEF.md
    ├── Handoff/
    └── Agents/          ← Empty, ready for activation
```

---

## Setup Steps

1. **Understand the project** — What are we building? What phase? Current documentation state?
2. **Identify relevant agents** — Check `/Agent Framework/Agents/` for available agents. Which does this project need?
3. **Activate agents** — For each needed agent, create their folder (see below)
4. **Populate the framework** — Fill PROJECT BRIEF, add tasks to agent TODOs, capture conventions
5. **Confirm with the human** — Review what was captured, ask what's missing

---

## Activating an Agent

To activate a framework agent (e.g., Developer, Writer):

1. Check the template at `/Agent Framework/Agent Data/Agents/[Agent Name]/` for the correct structure
2. Create `/Agent Data/Agents/[Agent Name]/` with:
   - `PROJECT INSTRUCTIONS - [Agent Name].md` (copy from template or start empty)
   - `TODO - [Agent Name].md` (copy from template or start empty)
   - `Reports/` folder
   - `Reports/Archive/` folder

The agent's GUIDING PRINCIPLES and REFERENCE files already exist in `/Agent Framework/Agents/[Agent Name]/`.

**Only active agents (those with folders in Agent Data) get their GUIDING PRINCIPLES read.** This keeps Claude focused on agents the project actually uses.

---

## Creating Custom Agents

For agents not in the framework (e.g., Vibe Checker, Dungeon Master):

Create everything in `/Agent Data/Agents/[Agent Name]/`:
- `GUIDING PRINCIPLES - [Agent Name].md` — Role definition and core principles
- `REFERENCE - [Agent Name].md` — Optional detailed guidance
- `PROJECT INSTRUCTIONS - [Agent Name].md` — Project-specific notes
- `TODO - [Agent Name].md` — Active tasks
- `Reports/` and `Reports/Archive/` folders

**Why Agent Data?** Custom agent definitions live in Agent Data so they're preserved when the framework is updated. Agent Framework gets replaced; Agent Data stays.

### Custom Agent Template

```markdown
# [Agent Name] — Guiding Principles

[One-line description of what this agent owns]

## Role

- [Responsibility 1]
- [Responsibility 2]
- [etc.]

## Core Principles

### [Principle Name]
[Brief explanation]

### [Principle Name]
[Brief explanation]

## Collaboration

- **[Other Agent]** — [How they work together]
```

---

## After Setup

Once Agent Data is in place with active agents, return to `CLAUDE.md` for ongoing work instructions.

# Agent Framework Instructions

Welcome, Claude. This document defines how you operate within this Agent Framework.

**Be concise.** Don't narrate what you're doing — just do it. Don't summarize these instructions back to the human. Read the files, check setup status, and get to work.

---

## Overview

This framework organizes work through **Agents** — specialized roles you can assume to focus on specific types of tasks. Each Agent has its own instructions, todo list, and reporting system.

---

## Core Principles

1. **Read this file first** on any new session — don't work from a summary
2. **Check PROJECT BRIEF.md** for current project context and goals
3. **Assume Agent roles as needed** — you can switch between Agents or work as multiple Agents collaboratively
4. **Maintain state** through Agent TODO lists and Reports
5. **Archive completed work** — Reports move to Archive folders when done

### On Conversation Compression
When a conversation is compressed and continued, **you must re-read this file**, plus:
- `/Agents/Shared/INSTRUCTIONS - Shared.md`
- `/Agents/Shared/PROJECT BRIEF.md`
- GUIDING PRINCIPLES and PROJECT INSTRUCTIONS for any active agents

Do not rely on summaries of these instructions — always read the source. The full instructions contain nuance that summaries lose.

If you've already read the instructions in this session (without being asked), let the human know briefly: "Already up to date on the framework instructions."

---

## First-Time Setup

**Check `/Agents/Shared/Setup/config.json`.** If the file is missing or `setupComplete` is `false`, this framework hasn't been configured yet.

### Check for Existing Project Data

Before starting fresh setup, check if there's already project information in the folder:
- Does `PROJECT BRIEF.md` have content beyond the template?
- Do any TODO files have tasks?
- Do any PROJECT INSTRUCTIONS files have project-specific content?

**If you find existing data but `setupComplete` is `false`:** Alert the human. Ask whether they want to:
1. **Integrate** — keep the existing content and continue setup from there
2. **Start fresh** — clear the project-specific content and begin new setup

This can happen when the framework was copied from another project or partially set up.

### If Setup Is Needed

Work with the human to onboard the project:

1. **Understand the project**
   - What are we building?
   - What phase is it in? (planning, building, testing, launched)
   - What's the current state of documentation?

2. **Identify relevant agents**
   - Check `/Agents/` to see what's available
   - Which agents does this project need?
   - Are there specialized roles that need new agents?

3. **Review existing documentation**
   - Are there existing TODO lists, task trackers, or backlogs? → Convert to Agent TODOs
   - Are there design docs, technical specs, or decisions? → Add to PROJECT INSTRUCTIONS
   - Are there style guides, conventions, or preferences? → Add to relevant agents
   - Is there a project overview or brief? → Populate PROJECT BRIEF.md

4. **Populate the framework**
   - Fill in PROJECT BRIEF.md with project context
   - Add existing tasks to relevant Agent TODO files
   - Capture known conventions in PROJECT INSTRUCTIONS files
   - Note any immediate priorities

5. **Confirm with the human**
   - Review what was captured
   - Ask what's missing
   - Clarify which agent to start working as

6. **Update config.json**
   - Once setup is complete, set `setupComplete` to `true` in `/Agents/Shared/Setup/config.json`
   - This signals to future sessions that the framework is configured

### The Goal

By the end of setup, the framework should reflect the project's current state — not start from scratch. Existing knowledge should live in the right places so future sessions can pick up where things left off.

---

## Working with the Human

**Collaborate, don't assume.**

- **Ask before diving deep.** If a task has multiple directions, check in before going down a rabbit hole. Confirm what they want.
- **Notice patterns.** If the human requests the same things repeatedly, that's a signal. Codify their workflow into Agent instructions or `/Agents/Shared/` so you build institutional knowledge.
- **Get feedback early.** Complete a small piece, show it, adjust. Don't build a mansion when they wanted a shed.
- **Stay focused.** Do what was asked. Add features, explanations, or tangents only when requested.
- **When uncertain, ask.** A quick clarifying question beats wasted effort.

---

## Folder Structure

```
/[Project]/Agent Framework/
├── INSTRUCTIONS - Claude.md              ← You are here (start every session by reading this)
└── Agents/
    ├── Shared/                           ← Shared resources across all Agents
    │   ├── INSTRUCTIONS - Shared.md      ← Universal guidelines for all Agents
    │   ├── PROJECT BRIEF.md              ← Current project context and goals
    │   └── Setup/
    │       └── config.json               ← Framework configuration
    └── [Agent Name]/
        ├── GUIDING PRINCIPLES - [Agent Name].md  ← Immutable role, skills, guidelines
        ├── PROJECT INSTRUCTIONS - [Agent Name].md ← Living project-specific notes
        ├── TODO - [Agent Name].md                 ← Active tasks for this Agent
        ├── Tools/                                 ← (optional) Local tools created by agent
        ├── Personas/                              ← (Testers only) User personas for testing
        └── Reports/
            ├── [Active reports]
            └── Archive/                           ← Completed/historical reports
```

### Two Types of Agent Instructions

Each Agent has two instruction files:

- **GUIDING PRINCIPLES** — Immutable by default. Defines the Agent's role, skills, and core guidelines. Can be changed at the human's explicit request.
- **PROJECT INSTRUCTIONS** — Living document. Captures project-specific conventions, decisions, and learnings. Update this as you work.

---

## How to Work as an Agent

### Starting a Session
1. Read this file (done!)
2. Read `/Agents/Shared/INSTRUCTIONS - Shared.md` for universal guidelines
3. Read `/Agents/Shared/PROJECT BRIEF.md` for context
4. Check `/Agents/` to see available Agents
5. Read the relevant Agent's `GUIDING PRINCIPLES - [Agent Name].md`
6. Read their `PROJECT INSTRUCTIONS - [Agent Name].md` for project-specific context
7. Review their `TODO - [Agent Name].md` for pending tasks

### While Working
- Stay in character for the Agent role
- Update `TODO - [Agent Name].md` as you complete tasks
- Create Reports in the Agent's `/Reports/` folder for significant outputs
- Reference other Agents when their expertise is needed

### Completing Work
- Mark TODO items as complete
- Move finished Reports to `/Archive/` with date prefix
- Update `/Agents/Shared/PROJECT BRIEF.md` if project status changes

### Building Institutional Knowledge
- When you learn something useful (workflow, preference, hard-won discovery), update the relevant Agent's `PROJECT INSTRUCTIONS - [Agent Name].md`
- Shared learnings that apply to all Agents go in `/Agents/Shared/`
- Capture good lessons — write them down
- Keep GUIDING PRINCIPLES files stable; update PROJECT INSTRUCTIONS freely

### Capturing Examples
When the human gives feedback, capture concrete examples in PROJECT INSTRUCTIONS:
- **Before/after pairs** — what was wrong, what fixed it
- **Positive examples** — "this is the quality bar"
- **Negative examples** — "this missed the mark, here's why"

Examples document the human's preferences better than abstract principles. They show what a guideline means *for this project*.

### Writing Instructions Positively
When the human gives feedback or corrections, codify it as **positive guidance** (carrots, not sticks):

- **Frame as "do this"** rather than "don't do that"
- **Use "before/after"** instead of "bad/good" for examples
- **State what works** rather than what fails
- **Encourage** rather than scold

The goal is instructions that inspire good work, not ones that warn against mistakes.

---

## Available Agents

Check the `/Agents/` folder to see which agents are available. Each subfolder (except `Shared/`) is an agent.

**You may not need all agents for any given project.** Use what's relevant.

### Matching Agents to the Project
At the start of a project, ask the human what the project needs. They may:
- Identify which existing agents are relevant
- Suggest new agents for this project's specific needs
- Have specialized roles in mind

### Use the Project Manager
When coordinating work across agents or tracking overall progress, **work as the Project Manager agent** rather than doing PM work as "yourself." This keeps responsibilities clear and documentation in the right place.

---

## Agent Collaboration

Agents can work together. For example:
- **Developer** might request validation from **QA**
- **Researcher** might hand off findings to **Writer**
- **Project Manager** coordinates between agents and tracks status

When switching Agents, read their `GUIDING PRINCIPLES - [Agent Name].md` and `PROJECT INSTRUCTIONS - [Agent Name].md` to adopt their perspective and expertise.

---

## Creating New Agents

To add a new Agent:
1. Create folder: `/Agents/[Agent Name]/`
2. Add `GUIDING PRINCIPLES - [Agent Name].md` with their role, skills, and core guidelines
3. Add `PROJECT INSTRUCTIONS - [Agent Name].md` for project-specific notes (can start empty)
4. Add empty `TODO - [Agent Name].md`
5. Create `/Reports/` and `/Reports/Archive/` folders

---

## Session Checklist

- [ ] Read INSTRUCTIONS - Claude.md (this file)
- [ ] Read /Agents/Shared/INSTRUCTIONS - Shared.md
- [ ] Read /Agents/Shared/PROJECT BRIEF.md
- [ ] Identify which Agent(s) to work as
- [ ] Read Agent's GUIDING PRINCIPLES - [Agent Name].md
- [ ] Read Agent's PROJECT INSTRUCTIONS - [Agent Name].md
- [ ] Check Agent's TODO - [Agent Name].md
- [ ] Do the work
- [ ] Update TODO - [Agent Name].md
- [ ] Update PROJECT INSTRUCTIONS - [Agent Name].md with learnings
- [ ] Create/archive Reports as needed

---

*Last updated: 2026-01-24*

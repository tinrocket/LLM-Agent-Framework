# Agent Framework

**Developed by:** John Balestrieri, [Tinrocket, LLC](https://www.tinrocket.com)
**License:** MIT

A structured framework for working with Claude and other LLMs on complex, multi-session projects.

## Why This Exists

Working with LLMs on real projects can get messy. Context gets lost between sessions, decisions aren't documented, and there's no consistent way to pick up where you left off.

The Agent Framework solves this by giving Claude a clear structure to operate within — specialized roles (Agents), persistent TODO lists, project documentation, and guidelines that maintain quality and consistency across sessions.

## How It Works

The framework organizes work through **Agents** — specialized roles Claude can assume to focus on specific tasks. Each Agent has:

- **Guiding Principles** — immutable rules defining the role
- **Project Instructions** — living document for project-specific notes and learnings
- **TODO list** — persistent task tracking
- **Reports** — documentation of significant work

Core agents include **Developer** and **Project Manager**, with optional agents for QA, Writing, Design, and more.

**Production-tested agents:** Developer, Project Manager, Writer, Game & Interaction Designer, QA, Testers. The remaining agents have been fleshed out for completeness but haven't seen production use yet.

## Installation

1. Copy the `Agent Framework` folder into your project
2. Point Claude at `INSTRUCTIONS - Claude.md` at the start of a session
3. Claude will detect it's a fresh setup and walk you through configuration

That's it. The framework lives in your project folder and persists between sessions.

## Usage

**Starting a session:**
Ask Claude to read the Agent Framework instructions. It will:
- Check if setup is complete
- Read the project brief and relevant agent instructions
- Pick up where the last session left off

**During work:**
- Claude works as specific Agents (Developer, PM, etc.)
- Tasks are tracked in Agent TODO files
- Learnings are captured in Project Instructions
- The human stays in control of priorities and direction

**Key principles:**
- Claude stays in scope — does what's asked, flags other issues for later
- One thing at a time — new requests get queued, not started immediately
- Institutional knowledge — patterns and preferences get documented for future sessions

## Session Handoff

**When a session gets slow, buggy, or glitchy** — ask Claude to create a handoff. This saves the current state (what was being worked on, recent decisions, next steps) to a file that the next session will pick up automatically.

Just say: *"Create a handoff"*

The next Claude instance will read the handoff, summarize it, and ask if you want to continue from there. No context lost.

## Structure

```
/Agent Framework/
├── INSTRUCTIONS - Claude.md      ← Start here
└── Agents/
    ├── Shared/                   ← Project brief, shared guidelines
    ├── Developer/                ← Technical implementation
    ├── Project Manager/          ← Coordination and tracking
    └── [Other Agents]/           ← QA, Writer, Designer, etc.
```

## Requirements

- Claude (Anthropic) — tested with Claude 4
- A project folder Claude can access

## Contributing

Pull requests and ideas welcome at [github.com/tinrocket/LLM-Agent-Framework](https://github.com/tinrocket/LLM-Agent-Framework)

## Disclaimer

This framework is provided without warranty. Always use version control and review the AI's work.

## License

MIT

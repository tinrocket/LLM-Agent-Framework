# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.2.0] - 2026-01-28

**Focus: Efficiency & Flexibility**

Claude now reads less on startup and only loads agents you actually use. Custom agents survive framework updates.

### Highlights
- **Faster startup** — CLAUDE.md slimmed from ~230 to ~160 lines; agent files cut in half
- **Gradual disclosure** — Detailed examples moved to REFERENCE files, read only when needed
- **Active agents only** — Only agents with folders in Agent Data get loaded
- **Custom agents preserved** — Create your own agents (Vibe Checker, Dungeon Master) in Agent Data; they won't be overwritten on updates
- **Cleaner setup** — New projects start with an empty Agents folder; activate only what you need

### Changed
- Split all 13 agent GUIDING PRINCIPLES into lean core (~35-40 lines) + REFERENCE files
- Setup now creates empty `Agents/` folder instead of copying all agent templates
- Renamed `SETUP.md` → `REFERENCE - Setup.md` for consistent naming
- Moved handoff template to `REFERENCE - Handoff.md`

### Added
- `REFERENCE - [Agent].md` files for all 13 agents (examples, templates, checklists)
- `REFERENCE - Setup.md` — first-time installation instructions
- `REFERENCE - Handoff.md` — handoff template
- Support for custom agents with GUIDING PRINCIPLES in Agent Data

## [1.1.0] - 2026-01-28

**Focus: Clean Separation & Easy Updates**

Your project data is now completely separate from framework files. Updating is drag-and-drop — just replace the Agent Framework folder.

### Highlights
- **No-merge updates** — Delete old `Agent Framework/`, drop in new one. Done.
- **Your work is safe** — TODOs, Reports, PROJECT INSTRUCTIONS all live in `Agent Data/`, untouched by updates
- **Simpler detection** — Framework checks for `Agent Data/` folder instead of config files
- **PM coordinates multiple agents** — New multi-agent consultation workflow

### Changed
- Split into `Agent Framework/` (immutable) and `Agent Data/` (your stuff)
- Entry point renamed to `CLAUDE.md`
- Business agent → Business & Marketing with messaging responsibilities

### Added
- README screenshot showing PM coordinating with Marketing, Writer, and Developer

### Removed
- `Setup/config.json` — no longer needed

### Migration
- See UPGRADING.md for steps from v1.0.x

## [1.0.2] - 2026-01-25

### Changed
- "Already up to date" message now asks if the framework has been updated before skipping re-read

## [1.0.1] - 2026-01-25

### Added
- Session handoff system for switching to fresh instances when sessions degrade
- Handoff folder structure (`/Agents/Shared/Handoff/` with `/Archive/`)
- `.gitkeep` files for all empty folders (Reports, Archive, Personas, Handoff)

## [1.0.0] - 2026-01-25

### Added
- Initial release
- Core framework with `INSTRUCTIONS - Claude.md` entry point
- Shared guidelines (`INSTRUCTIONS - Shared.md`)
- Project Brief template
- Setup configuration with `setupComplete` flag
- First-time setup flow with existing project detection
- 13 agents: Project Manager, Developer, QA, Writer, Game & Interaction Designer, Art Director, Audio, Testers, Researcher, Business, Community, Support, Compliance
- Two-file agent structure: GUIDING PRINCIPLES (immutable) + PROJECT INSTRUCTIONS (living)
- Persona-based testing system with example template
- Before/after examples in key agent guidelines
- Scope management: stay in scope, one thing at a time, queue new requests
- Local tools preference guideline
- Conversation compression protocol
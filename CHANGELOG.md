# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.1.0] - 2026-01-28

### Changed
- Restructured folder layout to separate framework files from user data
- Framework files now in `Agent Framework/` (GUIDING PRINCIPLES, shared instructions)
- User data now in `Agent Data/` (PROJECT INSTRUCTIONS, TODOs, Reports, config)
- Entry point renamed from `INSTRUCTIONS - Claude.md` to `CLAUDE.md`
- Updating now requires only replacing `Agent Framework/` folder — no merging

### Migration
- See UPGRADING.md for migration steps from v1.0.x

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
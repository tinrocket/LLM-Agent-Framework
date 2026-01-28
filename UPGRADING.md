# Upgrading the Agent Framework

## Quick Upgrade (v1.1+)

Starting with version 1.1, upgrading is simple:

1. Delete your `Agent Framework/` folder
2. Copy in the new `Agent Framework/` folder
3. Done

Your `Agent Data/` folder is untouched. No merging required.

## What Gets Replaced

The `Agent Framework/` folder contains:
- `INSTRUCTIONS - Shared.md`
- `Agents/[Agent Name]/GUIDING PRINCIPLES - [Agent Name].md`

## What's Preserved

The `Agent Data/` folder contains your project-specific data:
- `PROJECT BRIEF.md`
- `Setup/config.json`
- `Handoff/` folder
- `Agents/[Agent Name]/PROJECT INSTRUCTIONS - [Agent Name].md`
- `Agents/[Agent Name]/TODO - [Agent Name].md`
- `Agents/[Agent Name]/Reports/`

## Adding New Agents from an Update

If a new version includes agents you want:
1. Copy the agent folder to `Agent Framework/Agents/`
2. Create matching folder in `Agent Data/Agents/` with:
   - `PROJECT INSTRUCTIONS - [Agent Name].md`
   - `TODO - [Agent Name].md`
   - `Reports/Archive/`

## Removing Agents

Delete the agent's folder from both:
- `Agent Framework/Agents/[Agent Name]/`
- `Agent Data/Agents/[Agent Name]/`

## Upgrading from v1.0.x

If you're upgrading from the old single-folder structure:

1. Back up your project folder
2. Your old structure had everything in `Agent Framework/Agents/`
3. Move your user data files to the new `Agent Data/` structure:
   - `PROJECT BRIEF.md` → `Agent Data/`
   - `Setup/` → `Agent Data/Setup/`
   - `Handoff/` → `Agent Data/Handoff/`
   - `PROJECT INSTRUCTIONS - *.md` → `Agent Data/Agents/[Agent]/`
   - `TODO - *.md` → `Agent Data/Agents/[Agent]/`
   - `Reports/` → `Agent Data/Agents/[Agent]/Reports/`
4. Delete the old `Agent Framework/` folder
5. Copy in the new `Agent Framework/` folder

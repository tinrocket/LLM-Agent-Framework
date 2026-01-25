# Upgrading the Agent Framework

When a new version of the Agent Framework is released, follow these steps to upgrade while preserving your project-specific data.

## Files to Replace

These contain the framework logic and should be replaced with the new version:

- `INSTRUCTIONS - Claude.md`
- `Agents/Shared/INSTRUCTIONS - Shared.md`
- `GUIDING PRINCIPLES - [Agent Name].md` for each agent

## Files to Keep

These contain your project-specific data and should NOT be replaced:

- `Agents/Shared/PROJECT BRIEF.md`
- `Agents/Shared/Setup/config.json`
- `PROJECT INSTRUCTIONS - [Agent Name].md` for each agent
- `TODO - [Agent Name].md` for each agent
- Everything in `/Reports/` folders
- Everything in `/Tools/` folders
- Everything in `/Personas/` folder (Testers agent)

## Upgrade Steps

1. Back up your project folder
2. Download the new framework version
3. Replace the framework files listed above
4. Review the CHANGELOG for any breaking changes
5. If new agents were added, copy their folders if you want them

## Adding New Agents from an Update

If a new version includes agents you want:
1. Copy the entire agent folder to your `/Agents/` directory
2. The agent will be available immediately

## Removing Agents

Delete the agent's folder from `/Agents/`. The framework dynamically reads available agents from the folder structure.

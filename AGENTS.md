# AGENTS.md

## Purpose
This repository contains a reusable GitHub Copilot customization starter for teams that want to organize prompts, instructions, and agent guidance in a clean, maintainable structure.

Coding agents should keep the repository easy to understand, easy to reuse, and aligned with officially supported GitHub Copilot customization patterns.

## Repository overview
Key areas:
- `AGENTS.md` — repository-wide agent workflow guidance
- `.github/copilot-instructions.md` — global Copilot instructions
- `.github/instructions/` — path-specific instructions
- `.github/prompts/` — reusable prompt files
- `docs/` — human-readable setup and usage documentation

## Working model
Before making changes:
1. Read `AGENTS.md`
2. Read `.github/copilot-instructions.md`
3. Review relevant files in `.github/instructions/`, `.github/prompts/`, and `docs/`
4. Keep the customization structure consistent and easy to copy into other repositories

## Change boundaries
Prefer changes that:
- improve clarity
- improve maintainability
- stay close to official GitHub Copilot customization features
- avoid unnecessary custom conventions that depend on unsupported behavior

## Rules for changes
- Make the smallest change that solves the task.
- Preserve a clean starter-template structure.
- Prefer explicit, readable instructions over overly clever prompts.
- Keep examples practical and copy-paste friendly.
- Do not introduce repo-specific assumptions unless clearly documented.

## Documentation expectations
- Documentation should explain what each file is for.
- Prefer concise, actionable instructions.
- Separate agent-facing guidance from human-facing usage docs.
- When examples are provided, ensure they match the repository structure.

## Validation
When updating the repository:
- ensure file paths are correct
- ensure prompt, instruction, and documentation names are consistent
- ensure examples reference files that actually exist in the repository

## Expected output when summarizing work
When presenting changes, include:
- what files were added or updated
- why the structure is organized this way
- how a user should start using the repository

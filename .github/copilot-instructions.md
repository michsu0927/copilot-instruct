# Copilot Instructions

## Purpose
This repository is a starter template for organizing GitHub Copilot customization files using officially supported building blocks:
- `AGENTS.md`
- `.github/copilot-instructions.md`
- `.github/instructions/*.instructions.md`
- `.github/prompts/*.prompt.md`

## General guidance
- Prefer officially supported Copilot customization mechanisms over custom role-file conventions.
- Keep prompts focused on concrete tasks.
- Keep instructions reusable and scoped appropriately.
- Keep examples easy for teams to adapt to their own repositories.

## Repository conventions
- `AGENTS.md` contains agent workflow and repository working guidance.
- `.github/copilot-instructions.md` contains global guidance for the repository.
- `.github/instructions/` contains path-specific rules.
- `.github/prompts/` contains prompt entry points for common workflows.
- `docs/` contains human-readable explanations and onboarding material.

## Writing guidance
- Use clear headings.
- Prefer short sections with practical examples.
- Avoid unsupported claims about GitHub Copilot features.
- Distinguish official support from team conventions.

## Do not
- Do not treat prompt files as if they were permanent role switches.
- Do not describe `.github/agents/*.md` as an official GitHub Copilot standard unless explicitly documented.
- Do not mix human UI tutorials into agent-only files like `AGENTS.md`.

# copilot-instruct

[English](./README.md) | [繁體中文](./README.zh-TW.md)

A starter repository for organizing GitHub Copilot customization files with a clean, reusable structure.

This repository demonstrates how to combine:
- `AGENTS.md`
- `.github/copilot-instructions.md`
- `.github/instructions/*.instructions.md`
- `.github/prompts/*.prompt.md`

It is designed as a practical example and starter template for teams that want to build a structured Copilot customization setup without relying on unsupported role-file conventions.

## What this repository is for

Use this repository as a starting point if you want to:
- define repository-wide agent guidance
- add global Copilot instructions
- scope instructions to subsets of files
- create reusable prompt entry points for common workflows
- document how your team should adapt the setup

## What this repository is not

This repository is:
- not an official GitHub documentation mirror
- not a guarantee that every Copilot feature behaves identically in every IDE
- not a replacement for checking current GitHub documentation
- not based on `.github/agents/*.md` as an official standard

## Repository structure

```text
AGENTS.md
.github/
├── copilot-instructions.md
├── instructions/
│   ├── markdown.instructions.md
│   ├── rust.instructions.md
│   ├── instructions-folder.instructions.md
│   └── prompts-folder.instructions.md
└── prompts/
    ├── plan-change.prompt.md
    ├── implement-wrapper-change.prompt.md
    ├── review-change.prompt.md
    └── create-tests.prompt.md
docs/
└── copilot-customization-guide.md
```

## Suggested workflow

A simple prompt-based workflow for this repository is:

1. `/plan-change`
   - define the goal
   - identify impacted files
   - choose the smallest clean structure

2. `/implement-wrapper-change`
   - make the requested change
   - summarize what changed

3. `/review-change`
   - review clarity, correctness, and consistency

4. `/create-tests`
   - add validation guidance and usage notes

## How to adapt this template

1. Rewrite `AGENTS.md` for your repository.
2. Rewrite `.github/copilot-instructions.md` for your repo-wide conventions.
3. Replace instruction files with rules that match your real file types and directories.
4. Replace prompt files with workflows your team actually uses.
5. Update the documentation to explain your conventions clearly.

## Recommended next improvements

If you plan to share this repository publicly, consider these follow-up changes:
- rename prompts whose names still reflect an earlier repository context
- add repository topics and description on GitHub
- keep the guide aligned with current GitHub documentation over time

## Related documentation

See:
- `docs/copilot-customization-guide.md`
- `AGENTS.md`
- `.github/copilot-instructions.md`

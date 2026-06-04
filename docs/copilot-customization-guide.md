# Copilot Customization Guide

## Purpose
This repository demonstrates a clean GitHub Copilot customization layout based on:
- `AGENTS.md`
- `.github/copilot-instructions.md`
- `.github/instructions/*.instructions.md`
- `.github/prompts/*.prompt.md`

It is intended as a reusable starter for teams that want a structured customization setup without relying on unofficial role-file conventions.

## Recommended structure

```text
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
AGENTS.md
README.md
README.zh-TW.md
docs/
└── copilot-customization-guide.md
```

## What each file is for

### `AGENTS.md`
Repository-wide working guidance for coding agents.

Use it for:
- how agents should approach changes
- change boundaries
- validation expectations
- summary expectations

### `.github/copilot-instructions.md`
Global repository guidance for Copilot.

Use it for:
- general writing guidance
- repo-wide conventions
- supported terminology
- high-level constraints

### `.github/instructions/*.instructions.md`
Scoped instructions for subsets of files.

Use them for:
- file-type-specific guidance
- directory-specific rules
- narrow conventions that should not apply everywhere

Examples in this repository:
- `markdown.instructions.md` for Markdown documentation files
- `rust.instructions.md` for Rust source files
- `instructions-folder.instructions.md` for maintaining instruction files
- `prompts-folder.instructions.md` for maintaining prompt files

### `.github/prompts/*.prompt.md`
Reusable prompt entry points for common workflows.

Use them for:
- planning
- implementation
- review
- validation or usage guidance

## Suggested workflow

Instead of relying on unofficial role files such as `#architect.md` or `#developer.md`, prefer a prompt-based workflow like this:

1. `/plan-change`
   - define the goal
   - identify files involved
   - propose the smallest clean structure

2. `/implement-wrapper-change`
   - implement the requested change
   - summarize what was modified

3. `/review-change`
   - review correctness, clarity, and supported usage

4. `/create-tests`
   - add validation notes, usage checks, or example verification guidance

## Official support vs team conventions

A useful rule of thumb:
- Treat `AGENTS.md`, `.github/copilot-instructions.md`, `.github/instructions/*.instructions.md`, and `.github/prompts/*.prompt.md` as the supported foundation.
- Treat custom role-file patterns as optional team conventions, not as the primary supported model.

## How to adapt this repository

To adapt this starter for another repo:
1. keep the structure
2. rewrite `AGENTS.md` for the target repository
3. rewrite `.github/copilot-instructions.md` for repo-wide conventions
4. replace instruction files with repo-relevant scoped rules
5. replace prompts with workflows that match the actual project
6. keep both README files aligned if you maintain bilingual documentation

## Notes
- Keep prompts task-oriented.
- Keep instructions scoped.
- Keep AGENTS.md focused on agent workflow, not UI tutorials.
- Avoid unsupported claims about GitHub Copilot behavior.

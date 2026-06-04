---
applyTo: "**/*.rs"
---

# Rust Coding Guidelines

Follow idiomatic Rust and prefer clear, maintainable code.

## General rules

- Prefer readable code over clever abstractions.
- Keep functions focused and reasonably small.
- Follow existing naming and module patterns in the repository.
- Prefer explicit control flow when it improves readability.
- Reuse existing types and helpers before adding new ones.
- Keep error handling consistent with nearby code.
- Prefer returning structured errors instead of vague panic-style handling when errors are expected.
- Add or update tests when behavior changes.
- Keep feature-specific or platform-specific logic clearly separated when practical.

## Clippy guidance

Use Clippy as the baseline linting tool. Prefer code that passes standard Clippy checks cleanly.

Prioritize fixing lints in these categories:
- correctness
- suspicious
- style
- perf

Use extra care before enabling or enforcing:
- pedantic
- nursery
- restriction

These groups can be useful, but they often require project-specific judgment.

## Project lint preferences

Prefer avoiding patterns commonly flagged by Clippy, such as:
- needless clones
- avoidable allocations
- redundant closures
- manual patterns that have clearer standard-library alternatives
- APIs with `len()` but no `is_empty()` where appropriate

## Review checklist

When reviewing Rust code, check:
- is the code easy to read?
- does it match surrounding patterns?
- is error handling clear?
- are new abstractions truly necessary?
- does the change require tests or documentation updates?
- does the code align with the project's chosen Clippy expectations?

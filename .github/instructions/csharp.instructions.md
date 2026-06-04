---
applyTo: "**/*.cs"
---

# C# Coding Guidelines

Follow standard .NET and C# coding conventions, and prefer code that is easy to read, maintain, and adapt.

## General rules

- Prefer clear and consistent code over clever or overly compact expressions.
- Follow existing naming, project, and folder patterns in the repository.
- Use modern C# language features when they improve clarity.
- Avoid outdated language constructs when a clearer modern alternative exists.
- Only catch exceptions that can be handled meaningfully.
- Prefer specific exception types instead of catching general exceptions.
- Use `async` and `await` for I/O-bound operations when appropriate.
- Prefer language keywords for built-in types, such as `string`, `int`, and `bool`.
- Use `var` only when the type is obvious from the right-hand side.
- Keep methods focused and reasonably small.
- Add or update tests when behavior changes.

## Naming and structure

- Use `PascalCase` for type names, namespaces, and public members.
- Use `camelCase` for local variables and method parameters.
- Use meaningful names that describe intent.
- Keep one statement per line and one declaration per line when practical.
- Keep related responsibilities together and avoid mixing unrelated concerns in the same file.

## Style guidance

- Use four spaces for indentation and do not use tabs.
- Prefer consistent formatting that improves readability.
- Use Allman style braces, with opening and closing braces on their own lines.
- Break long statements into multiple lines when needed for clarity.
- Place line breaks before binary operators when wrapping expressions.
- Add blank lines between members when it improves scanability.

## String and collection guidance

- Prefer string interpolation over manual concatenation for short formatted strings.
- Use `StringBuilder` when building large strings in loops.
- Prefer collection and LINQ APIs when they improve readability without obscuring intent.
- Avoid unnecessary allocations and redundant transformations.

## Comments and documentation

- Use `//` comments for short explanations.
- Place comments on their own lines, not at the end of code lines.
- Use XML documentation comments for public types and public members when the repository uses them.
- Prefer self-explanatory code over excessive comments.

## Review checklist

When reviewing C# code, check:
- is the code easy to read and consistent with nearby code?
- are naming conventions followed?
- is exception handling specific and intentional?
- are async patterns used correctly where needed?
- does formatting follow standard .NET conventions?
- does the change require tests or documentation updates?

## Reference

These guidelines are aligned with Microsoft Learn C# coding conventions and naming guidance.

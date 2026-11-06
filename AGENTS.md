# Global Agent Instructions

## Collaboration

Language: Respond in Simplified Chinese by default. Retain English for code, technical terms, and references.

How to collaborate with me:

- I am a developer and prefer direct, practical communication.
- I may work on software, hardware, or combined hardware/software problems.
- I want solutions consistent with modern software engineering practices.
- My preferred languages are C/C++, C#, Python, PowerShell, and Bash.

## Autonomy

- Infer intent and scope from the user's request and available context.
- Favor action over clarification. Independently resolve routine ambiguity through investigation and engineering judgment.
- Treat ordinary, reversible work implied by the request as authorized. Avoid seek intermediate approval for implementation details.
- Ask when uncertain. Ask when an unresolved decision materially affects correctness, safety, or externally visible behavior and cannot be reasonably inferred.

## Safety and source control

- Protect credentials and other secrets. Do not include them in code or documentation, or expose them in logs or output.
- Preserve unrelated user changes. Stay within the authorization given when discarding work, rewriting shared history, or taking destructive or irreversible actions.
- Use Angular-style commit messages, in Chinese by default.

## Coding

- Follow the project's technology stack, configuration, and coding conventions unless the task justifies changing them.
- Follow modern software engineering principles and code styles. Make enginnering-friendly and engineer-friendly code.
- Investigate unknown requirements, hardware details, protocols using available code and documentation.
- Design maintainable APIs with clear interfaces and appropriate abstractions.
- DO NOT make defensive programming designs and defensive explain/description/documentation.
- Make the smallest/simplest implementation that satisfies the requested scope. DO NOT overdesign, DO NOT write unnecessary code and speculative edge cases.
- Make justified broader changes when necessary, without expanding into unrelated work.
- If you cannot validate locally, provide exact commands and explain what to check.

## Documentation

- Write documentation in Chinese and code comments in English by default.
- Keep documentation brief, and write concise, clear documentation that provides the most useful information for developers.
- Use `$humanizer-zh` and `$stop-slop` when writing documentation when applicable and available.

## Environment preferences

- Check the execution environment; do not assume it matches the host OS.
- Prefer UTF-8 for new text. Preserve existing encodings unless conversion is required.
- On Windows, prefer PowerShell 7 (`pwsh`) when available. Prefer `.ps1` scripts compatible with both PowerShell 7 and Windows PowerShell 5.1.
- Prefer CRLF on Windows and LF elsewhere by default. Follow `.gitattributes`, `.editorconfig`, and existing line endings.
- Prefer forward slashes (`/`) in paths, unless the target tool or API must requires backslashes (`\`).
# Global Agent Instructions

## Collaboration

- Respond in Simplified Chinese by default. Use English for code, technical terms, and references where appropriate.
- Be direct, precise, and practical. Challenge incorrect assumptions with technical reasons.

## Architecture

- you may work on software, hardware, or mix system problems.
- Respect architecture and contracts.
- Work within the project's established architecture: preserve module responsibilities, dependency direction, public interfaces, and existing mechanisms. Inspect the relevant code, call sites, and documentation before changing them; do not perform exhaustive repository exploration by default.
- Make necessary local refactors within those boundaries. Do not redesign module boundaries, introduce cross-layer dependencies, replace established mechanisms, or change technologies merely because doing so seems easier.
- Treat existing external contracts as protected. This includes wire protocols (frame layout, message IDs, field widths and order, endianness, encoding, checksums), public APIs/ABIs, serialized or persistent data formats, configuration schemas, and hardware interfaces or timing constraints.
- Do not change protected contracts unless the user explicitly requests that contract change. When implementing new functionality, preserve compatibility with existing participants and documented specifications. Never silently change a protocol frame to make an implementation or test pass.
- If the task cannot be completed correctly without changing a protected contract or architectural boundary, keep it intact and explain the specific blocker and proposed change instead of making the change unilaterally.

## Implementation Quality

- Follow the repository's toolchain, configuration, coding conventions, and relevant design patterns.
- Prefer the simplest correct and complete implementation that fits the existing architecture. Avoid speculative features, unrelated cleanup, and unnecessary abstraction; do not sacrifice required behavior or validation to minimize code size.
- Preserve necessary error handling, boundary checks, and input validation, especially around untrusted data, buffers, I/O, hardware, and protocol parsing. Avoid speculative defensive complexity, not essential correctness checks.
- Fix root causes. Do not alter specifications, tests, expected results, or existing contracts merely to conceal a failing implementation.

## Verification and Completion

- Check the diff for unintended changes, including effects on architecture and external behavior.
- Compile or type-check affected code and run relevant tests when feasible. Resolve failures caused by the change before reporting completion; avoid unnecessary full-suite runs when targeted checks suffice.
- For protocol or serialization work, verify against the existing specification and independent known-good frames or compatibility tests when available. A sender and receiver that agree only with each other do not establish protocol compatibility.
- State what was actually verified and what remains unverified. If local validation is unavailable, provide actionable checks; never claim success without evidence.

## Safety and Source Control

- Protect credentials and secrets; do not expose them in code, documents, logs, or outputs.
- Preserve unrelated user changes. Do not discard work, rewrite shared history, or perform destructive or irreversible actions outside explicit authorization.
- Follow the repository's commit conventions; otherwise use Angular-style commit messages, in Chinese by default.

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
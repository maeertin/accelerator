---
name: react-utils-ref
description: Use `@noaignite/react-utils` for ref composition, forwarding, and element ref helpers.
---

# react-utils-ref

Use this skill when a task involves multiple refs or forwarding refs safely.

## Use it for

- Combining refs with `useForkRef`
- Assigning refs with `setRef`
- Reading the underlying element ref with `getReactElementRef`

## Lookup rules

1. Resolve the installed `@noaignite/react-utils` package for the current consumer without assuming package manager layout.
2. Once resolved, stop broad searching and inspect that package directory directly.
3. Verify docs by listing `dist/docs/`, then read `dist/docs/<export>.md`, then `dist/<export>.d.ts` if needed.
4. If a lookup is unexpectedly empty, verify the resolved directory directly before concluding the docs are missing.

Guardrails:

- Do not use repo-wide `glob` or `grep` after the package path is known.
- Do not mix a full repo-relative glob pattern with a scoped `path`.
- Use web docs only when local docs and local type files are both unavailable.

## Good prompts

- “Forward this ref while keeping an internal ref too.”
- “Merge these refs onto the same element.”

---
name: react-utils-state
description: Use `@noaignite/react-utils` for controlled/uncontrolled state patterns, state synchronization, and value management.
---

# react-utils-state

Use this skill when a task is about component state that can be controlled or uncontrolled.

## Use it for

- Controlled and uncontrolled inputs or components
- Syncing internal state with external props
- State helpers such as `useControlled`

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

- “Make this component work in controlled and uncontrolled modes.”
- “Keep local state in sync with an incoming prop.”

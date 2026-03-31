---
name: react-utils-interaction
description: Use `@noaignite/react-utils` for dismissal, focus management, inert state, and press/hold interactions.
---

# react-utils-interaction

Use this skill when the task is about interaction flows and accessibility behavior.

## Use it for

- Dismissible overlays and outside-click handling
- Focus return after closing a surface
- Applying inert state to background content
- Press-and-hold or gesture-like interactions

## Lookup rules

1. Resolve the installed `@noaignite/react-utils` package for the current consumer without assuming package manager layout.
2. Once resolved, stop broad searching and inspect that package directory directly.
3. Verify docs by listing `dist/docs/`, then read `dist/docs/<export>.md`, then `dist/<export>.d.ts` if needed.
4. If a lookup is unexpectedly empty, verify the resolved directory directly before concluding the docs are missing.

Guardrails:

- Do not use repo-wide `glob` or `grep` after the package path is known.
- Do not mix a full repo-relative glob pattern with a scoped `path`.
- Use web docs only when local docs and local type files are both unavailable.

## Common hooks

- `useDismiss`
- `useFocusReturn`
- `useInert`
- `usePressHold`

## Good prompts

- “Close this menu when the user clicks outside.”
- “Return focus to the trigger after dismissing the dialog.”

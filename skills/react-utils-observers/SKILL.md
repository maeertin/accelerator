---
name: react-utils-observers
description: Use `@noaignite/react-utils` for viewport visibility, scroll-driven UI, resize, and DOM observer hooks.
---

# react-utils-observers

Use this skill for DOM observation and visibility-driven behavior.

## Use it for

- Viewport visibility and in-view/out-of-view state
- Scroll-into-view behavior and lazy reveal patterns
- Element size changes and layout measurement
- DOM mutation tracking

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

- `useIntersectionObserver`
- `useResizeObserver`
- `useMutationObserver`
- `useElementSize`

## Good prompts

- “Show different content when the element enters the viewport.”
- “Track when this card is visible while scrolling.”
- “Recompute layout when the container resizes.”

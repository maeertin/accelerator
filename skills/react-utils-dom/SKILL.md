---
name: react-utils-dom
description: Use `@noaignite/react-utils` for browser-safe DOM helpers, events, and viewport/window utilities.
---

# react-utils-dom

Use this skill when a task needs browser-aware helpers outside pure observer logic.

## Use it for

- Event helpers like `useEvent`
- SSR-safe effects like `useIsomorphicEffect`
- Viewport and window helpers like `useWindowSize` and `useVisualViewport`
- Responsive behavior like `useMediaQuery`
- Scroll and sticky utilities like `useScrollProgress` and `useSticky`

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

- “React to window size changes.”
- “Make this code safe in SSR.”

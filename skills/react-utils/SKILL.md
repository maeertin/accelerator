---
name: react-utils
description: Use `@noaignite/react-utils` in other repositories. Trigger when the user needs shared React hooks, utilities, or component helpers, wants to install or import the package, or is building reusable React logic that should come from the published npm package. For targeted tasks, route to the matching sub-skill such as `react-utils-state`, `react-utils-ref`, `react-utils-observers`, `react-utils-dom`, or `react-utils-interaction`.
---

# @noaignite/react-utils

Use this package when you need reusable React helpers that are safe to share across apps.

## Route to the right skill

- Use `react-utils-state` for controlled/uncontrolled state patterns and state sync.
- Use `react-utils-ref` for ref composition and forwarding.
- Use `react-utils-observers` for viewport visibility, resize, mutation, and scroll-driven UI.
- Use `react-utils-dom` for browser-safe DOM helpers, window/viewport sizing, and event helpers.
- Use `react-utils-interaction` for dismissal, focus return, inert, and press/hold flows.

## Lookup rules

1. Resolve the installed `@noaignite/react-utils` package for the current consumer without assuming package manager layout.
2. Once resolved, stop broad searching and inspect that package directory directly.
3. Verify docs by listing `dist/docs/`, then read `dist/docs/<export>.md`, then `dist/<export>.d.ts` if needed.
4. If a lookup is unexpectedly empty, verify the resolved directory directly before concluding the docs are missing.

Guardrails:

- Do not use repo-wide `glob` or `grep` after the package path is known.
- Do not mix a full repo-relative glob pattern with a scoped `path`.
- Use web docs only when local docs and local type files are both unavailable.

## What it provides

Use the package for:

- React hooks and browser-state helpers
- Controlled/uncontrolled state patterns
- DOM and observer utilities
- Ref helpers
- Small React component primitives

Common exports include:

- Components/helpers: `createPolymorph`, `createRenderBlock`, `createRequiredContext`, `createSvgIcon`, `ErrorBoundary`, `getReactElementRef`, `setRef`
- Hooks: `useControlled`, `useDismiss`, `useDragScroll`, `useElementSize`, `useEvent`, `useFocusReturn`, `useForkRef`, `useGesture`, `useInert`, `useIntersectionObserver`, `useInterval`, `useIsomorphicEffect`, `useMediaQuery`, `useMutationObserver`, `usePressHold`, `useResizeObserver`, `useRTL`, `useScrollProgress`, `useStableCallback`, `useSticky`, `useTimeout`, `useVisualViewport`, `useWindowSize`

## How to choose the right helper

- Use `useControlled` for components that can be either controlled or uncontrolled.
- Use `useForkRef` or `setRef` when multiple refs must point at the same element.
- Use `useEvent` or `useStableCallback` when callback identity matters.
- Use observer hooks (`useResizeObserver`, `useMutationObserver`, `useIntersectionObserver`) for DOM-driven UI state.
- Use `useMediaQuery`, `useVisualViewport`, or `useWindowSize` for responsive behavior.
- Use `useDismiss`, `useFocusReturn`, `useInert`, or `usePressHold` for interaction/accessibility flows.
- Use `createSvgIcon` for icon components and `createRequiredContext` for context APIs that should fail fast when misused.

## Implementation guidance

- Prefer the package’s abstractions over ad hoc hook code.
- Keep browser APIs guarded so code remains safe in SSR or non-DOM environments.
- Keep tests close to behavior, especially for hooks and observer-based utilities.
- If a feature needs a new helper, prefer adding it here only if it is genuinely reusable across apps.

## Good usage examples

- “Use `useMediaQuery` to switch layouts at a breakpoint.”
- “Use `createRequiredContext` so consumers get a clear error when the provider is missing.”
- “Use `useResizeObserver` instead of wiring a custom `ResizeObserver` in each app.”
- “Use `createPolymorph` when building a reusable component that supports an `as` prop.”

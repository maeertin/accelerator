---
name: react-utils
description: Use `@noaignite/react-utils` in other repositories. Trigger when the user needs shared React hooks, utilities, or component helpers, wants to install or import the package, or is building reusable React logic that should come from the published npm package.
---

# @noaignite/react-utils

Use this package when you need reusable React helpers that are safe to share across apps.

## Start here

- Install it with `pnpm add @noaignite/react-utils` (or the package manager the user prefers).
- Prefer the public exports from `@noaignite/react-utils` instead of reimplementing common hooks or helpers.
- Respect the peer dependency range: `react` and `react-dom` `^18 || ^19`.

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

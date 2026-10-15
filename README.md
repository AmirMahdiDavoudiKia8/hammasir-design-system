# Ham-Masir Design System

A standalone design system for Ham-Masir, built to keep the product’s UI consistent, accessible, and easy to maintain.

It brings together the design tokens, reusable components, and Storybook documentation in one place, while preserving the original project structure so existing `@/` aliases and relative imports continue to work without changes.

## What’s Inside

- **Design tokens:** `src/design-system/tokens/tokens.css` — the main source for colors, surfaces, and other design values, with support for light and dark themes.
- **Components:** `src/design-system/components/` — reusable UI components and their Storybook stories.
- **Foundations:** `src/design-system/foundations/` — documentation for the principles behind the visual system.
- **Component reference:** `src/design-system/README.md` — a full inventory of components, their status, and token usage.
- **AI maintenance guide:** `AI_MAINTENANCE_SKILL.md` — guidelines for AI tools working on the design system.

## Getting Started

Install the dependencies and run Storybook to explore the components locally.

```bash
npm install
npm run storybook
```

Storybook will be available at `http://localhost:6006`.

To check the project, run:

```bash
npm run typecheck
npm run build-storybook
```

The type check should complete without errors. The Storybook build generates a static version of the documentation in `storybook-static/`.

## Design Principles

A few principles guide the system and help keep the experience consistent across the product:

- **Calm by default:** Motion should feel subtle and purposeful, never distracting.
- **Whitespace matters:** Give content room to breathe and make interfaces easier to understand.
- **Stay true to the brand:** Avoid pure black and white, neon colors, and visual choices that feel out of place in Ham-Masir.
- **Designed for Persian:** RTL layouts and Persian numerals in user-facing content are part of the experience, not afterthoughts.
- **Accessible to everyone:** Components should support keyboard navigation, visible focus states, and screen readers.

The goal is simple: make it easier to build new parts of Ham-Masir without reinventing the same design decisions every time.

## Verification & Accessibility

The design system has been checked beyond basic code validation, with a focus on interactive behavior, theme consistency, and accessibility.

What Works

- Clean setup: A fresh installation was tested to check that the project builds without relying on hidden dependencies. Storybook controls and component props were also checked for correct types and expected value ranges.
- Light and dark themes: Components were tested in both themes, from individual elements to more complex compositions. Dark mode uses softer, less saturated colors to keep the interface comfortable to read.
- Keyboard navigation: Interactive form elements support keyboard navigation and visible focus states. Sheets can be dismissed with "Escape", by clicking the backdrop, or with a swipe gesture on mobile.
- Screen readers: "ThemeToggle" exposes its state through "aria-pressed". Toast notifications use the application Provider in Storybook and announce updates through "aria-live". Decorative input icons are hidden from assistive technologies, and Card compositions avoid nested interactive elements.
- RTL support: Layouts use logical CSS properties and an RTL context, allowing browser behavior to adapt naturally. For example, the Textarea resize handle moves to the bottom-left in RTL layouts without relying on fragile CSS overrides.

Known Limitations

A few details still need attention as the design system evolves:

- Alert status indicators: Alert variants currently rely mainly on background and border colors to communicate their meaning. Adding semantic icons will make these states easier to distinguish for people who have difficulty perceiving color differences.
- ProgressBar labels: "ProgressBar" is designed to stay visually minimal, particularly in multi-step headers. Its accessibility therefore depends on developers providing a meaningful "ariaLabel", which is required by the component's TypeScript props.
- Tag vs. Chip: "Tag" is intended for displaying information and is not interactive or keyboard-focusable. For selectable options or filtering, use "Chip" instead.

These checks help keep the system consistent and usable, while the known limitations provide a clear starting point for future improvements.

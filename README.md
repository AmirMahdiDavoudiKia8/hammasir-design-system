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

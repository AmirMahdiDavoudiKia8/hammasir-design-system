# Ham-Masir Design System (standalone)

Token-driven, RTL-first UI foundation for Ham-Masir — extracted as a
self-contained package. Same relative layout as the source monorepo, so every
`@/` import and every relative import works unchanged.

- Tokens: `src/design-system/tokens/tokens.css` (canonical, light + `.dark`)
- Components: `src/design-system/components/*` (15 folders, stories included)
- Foundations docs: `src/design-system/foundations/*.mdx`
- Full inventory, statuses and token roles: `src/design-system/README.md`
- Agent rules: `AI_MAINTENANCE_SKILL.md`

## Clean-checkout setup (verified commands)

```bash
npm install
npm run storybook         # visual review → http://localhost:6006
npm run build-storybook   # static build into storybook-static/
npm run typecheck         # tsc --noEmit, must pass clean
```

All four commands were executed against a clean clone during release
validation (typecheck clean, Storybook static build successful).

## Brand laws (non-negotiable)

Calm motion only, whitespace is trust, no pure black/white or neon, Persian
numerals in user-facing content, full keyboard and screen-reader support.

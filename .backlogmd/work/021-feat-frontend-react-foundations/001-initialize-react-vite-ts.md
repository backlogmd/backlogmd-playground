<!-- METADATA -->

```yaml
task: Initialize React app with Vite and TypeScript
status: in-progress
priority: 10
dep: []
assignee: "Jazmin"
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Create the frontend project with Vite, React 18, and TypeScript. Add base config (tsconfig, ESLint, path aliases) and a minimal entry point that renders the app shell.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [ ] New app in `frontend/` (or agreed folder); `npm run dev` and `npm run build` succeed
- [ ] TypeScript strict and ESLint run clean
- [ ] Path alias configured (e.g. `@/` for src)

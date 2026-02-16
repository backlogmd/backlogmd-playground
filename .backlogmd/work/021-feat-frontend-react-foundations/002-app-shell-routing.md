<!-- METADATA -->

```yaml
task: Add app shell and routing
status: open
priority: 20
dep: ["work/021-feat-frontend-react-foundations/001-initialize-react-vite-ts.md"]
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Set up React Router and a root layout: header/nav, main content area, and placeholder routes (e.g. `/`, `/rains`, `/trigger`). Ensure a single outlet for future pages.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [ ] Routes for `/`, `/rains`, `/trigger` with placeholder content
- [ ] Persistent shell (header + nav + main outlet)
- [ ] Nav links change route without full reload

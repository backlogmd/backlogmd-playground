<!-- METADATA -->

```yaml
task: Configure API client for Hamburger Rain API
status: open
priority: 30
dep: ["work/021-feat-frontend-react-foundations/001-initialize-react-vite-ts.md"]
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Create a small API client (fetch or axios) that uses base URL and API key from env (e.g. `VITE_API_BASE_URL`, `VITE_API_KEY`). Expose typed helpers for `POST /rain` and `GET /rain/:id` (or a minimal subset).

<!-- ACCEPTANCE -->

## Acceptance criteria

- [ ] Env-based config (VITE_API_BASE_URL, VITE_API_KEY); client sends API key on requests
- [ ] Typed helpers for trigger rain and get rain status
- [ ] Can call real API or mock; no hardcoded secrets

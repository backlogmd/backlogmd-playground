<!-- METADATA -->

```yaml
task: Add E2E tests for rain API
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

E2E tests: create rain with API key, poll until completed, assert response shape.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] E2E: POST /rain then GET /rain/:id until completed
- [x] E2E: 401 without valid key, 429 when over limit
- [x] Run in CI against test deployment

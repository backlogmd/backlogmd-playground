<!-- METADATA -->

```yaml
task: Implement rate limiting per API key
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Apply rate limits (e.g. 100 req/min per key) and return 429 when exceeded.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] Limits applied per API key
- [x] 429 with Retry-After when limit exceeded
- [x] Limit configurable via env

<!-- METADATA -->

```yaml
task: Implement POST /rain endpoint
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Accept a rain request, validate params, enqueue job, return rain ID and status URL.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] POST /rain creates a rain job
- [x] Request body validated (intensity, types, optional region)
- [x] Response 202 with Location and rain id

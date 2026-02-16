<!-- METADATA -->

```yaml
task: Implement GET /rain/:id endpoint
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Return current status, progress, and ETA for a given rain id.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] GET /rain/:id returns status and metadata
- [x] 404 when rain id not found
- [x] Response includes startedAt, completedAt when applicable

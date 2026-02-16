<!-- METADATA -->

```yaml
task: Add intensity parameter to rain API
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Accept intensity in POST /rain and pass it to the rain engine.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] Enum: drizzle, light, moderate, heavy, storm
- [x] Default: moderate when omitted
- [x] Invalid value returns 400 with message

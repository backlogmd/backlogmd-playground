<!-- METADATA -->

```yaml
task: Implement rain events analytics
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Store and expose aggregate counts: rains per tenant, per day, by status.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] Increment counters on rain created/completed
- [x] GET /analytics/rain-counts (scoped by API key)
- [x] Optional query: by date range

<!-- METADATA -->

```yaml
task: Add monitoring and alerting
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Instrument API and rain service; dashboards and alerts for errors and latency.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] Metrics: request count, latency, rain job queue depth
- [x] Dashboard for key metrics
- [x] Alert when error rate or latency exceeds threshold

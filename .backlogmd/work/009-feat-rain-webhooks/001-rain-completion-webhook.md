<!-- METADATA -->

```yaml
task: Implement rain completion webhook
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

On rain completion or failure, POST to client-provided webhook URL.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] Optional webhookUrl in POST /rain
- [x] POST to URL with rainId, status, completedAt
- [x] Retry with backoff on 5xx (documented)

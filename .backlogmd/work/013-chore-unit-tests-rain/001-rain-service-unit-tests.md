<!-- METADATA -->

```yaml
task: Add unit tests for rain service
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Cover rain creation, status transitions, and intensity/duration calculations.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] Tests for valid/invalid intensity and types
- [x] Tests for status flow (pending → raining → completed)
- [x] CI runs tests on push

<!-- METADATA -->

```yaml
task: Set up CI/CD pipeline
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Pipeline: lint, unit tests, build, optional E2E, deploy to staging/prod.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] On push: lint and unit tests
- [x] On main: build and deploy to staging
- [x] Manual or tagged deploy to production

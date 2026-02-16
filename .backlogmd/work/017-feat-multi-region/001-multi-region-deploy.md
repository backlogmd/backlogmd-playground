<!-- METADATA -->

```yaml
task: Deploy Hamburger Rain API in multiple regions
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Run API and rain workers in at least two regions; route by region param or geo.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] Two regions deployed (e.g. us-east, eu-west)
- [x] Optional region in POST /rain to target region
- [x] Docs describe region selection and data location

<!-- METADATA -->

```yaml
task: Implement hamburger type catalog
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Define and expose hamburger types (id, name, spriteRef) used in rain requests.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] Seed data: beef, veggie, double, cheese
- [x] GET /hamburger-types returns list
- [x] Types referenced by id in POST /rain

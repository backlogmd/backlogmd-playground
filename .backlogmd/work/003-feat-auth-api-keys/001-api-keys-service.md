<!-- METADATA -->

```yaml
task: Implement API key generation and validation
status: done
priority: 10
dep: []
assignee: ""
requiresHumanReview: false
expiresAt: null
```

<!-- DESCRIPTION -->

## Description

Build the auth layer: create, store, and validate API keys for clients.

<!-- ACCEPTANCE -->

## Acceptance criteria

- [x] Generate and persist API keys
- [x] Middleware validates key and attaches tenant to request
- [x] Invalid/missing key returns 401

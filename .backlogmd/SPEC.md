# Backlogmd SPEC (v4.0.4)

Single source of truth for the `.backlogmd/` folder. Agents and tools should follow this spec when reading or writing backlog content.

## Directory structure

```
.backlogmd/
├── work/
│   ├── <item-id>-<slug>/
│   │   ├── index.md
│   │   ├── 001-task-slug.md
│   │   ├── 001-task-slug-feedback.md   # optional
│   │   └── ...
│   └── ...
├── z-archive/
│   └── <YYYY>/<MM>/<item-id>-<slug>/
└── SPEC.md (this file)
```

All paths are relative within `.backlogmd/`.

## Open items

- **Open items** are directories under `work/`. Discover tasks by listing each item dir for `<tid>-<task-slug>.md`.
- **Item status:** `plan` | `open` | `claimed` | `in-progress` | `done`. Items with `status: open` or `claimed` may have tasks ready to start.
- **Archived items** live under `z-archive/<YYYY>/<MM>/`; agents ignore them for active work.
- When every task in an item is `done`, archive by moving the item folder to `z-archive/<YYYY>/<MM>/<item-id>-<slug>/`.

## IDs and naming

- **Item IDs:** Zero-padded, min 3 digits (e.g. `001`, `012`). Unique across the backlog.
- **Task IDs:** Zero-padded, min 3 digits. Unique per item.
- **Slugs:** Lowercase kebab-case. Optional type prefix (e.g. `feat`, `chore`) in slug.
- **Priority:** Integer per item. Lower number = higher priority.

## Item format (`work/<item-id>-<slug>/index.md`)

Required blocks: `<!-- METADATA -->`, `<!-- DESCRIPTION -->`, `<!-- CONTEXT -->`.

**METADATA YAML:**

```yaml
work: <work item title>
status: plan | open | claimed | in-progress | done
assignee: ""   # agent id when status is claimed; empty when open or done
```

- **Work-level assignee:** Required when `status: claimed`; set when claiming; clear when releasing or when item is `done`.

## Task format (`work/<item-id>-<slug>/<tid>-<task-slug>.md`)

Required blocks: `<!-- METADATA -->`, `<!-- DESCRIPTION -->`, `<!-- ACCEPTANCE -->`.

**METADATA YAML:**

```yaml
task: <task title>
status: plan | open | in-progress | review | block | done
priority: <integer>
dep: []   # optional paths relative to .backlogmd/
assignee: ""
requiresHumanReview: false
expiresAt: null
```

- `in-progress` and `review` require non-empty `assignee`; `done` must have empty `assignee`.
- **dep:** Paths like `work/<item-id>-<slug>/<tid>-<task-slug>.md`. DAG only; no cycles.

## Status flow

- **Item:** `plan` → `open` → `claimed` → `in-progress` → `done` (when all tasks done).
- **Task:** `plan` → `open` → `in-progress` → `done` (or `review` → `done` if human review). Any active → `block` → `open` or `in-progress`.

## Archive

- Archive only when **every** task in the item has `status: done`.
- Move folder to `z-archive/<YYYY>/<MM>/<item-id>-<slug>/`. Do not modify after archiving.

## Limits

- Max **20** open items (max 20 directories in `work/`).
- Recommended max 20 tasks per item.

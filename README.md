# backlogmd-playground

A **playground space** for testing the [backlogmd](.agents/skills/backlogmd/SKILL.md) skill and how it handles the `.backlogmd/` folder.

## Purpose

- **Exercise the backlogmd skill** — Create items, tasks, start/done flows, archive, and sanity checks.
- **Validate the backlog structure** — Ensure `.backlogmd/work/` and `.backlogmd/z-archive/` behave as the skill expects (e.g. max 20 open items, task deps, status transitions).
- **No production app** — The repo may contain example work (e.g. the fictional “Hamburger Rain API” backlog) purely to stress-test the skill; the codebase itself is not the goal.

## Layout

- **`.backlogmd/`** — Backlog root: `work/` (open items), `z-archive/` (archived items). Managed by the backlogmd skill.
- **`.agents/skills/backlogmd/`** — The backlogmd skill definition (SKILL.md) used by agents to operate on `.backlogmd/`.

Use the backlogmd skill to plan work, start tasks, mark them done, and archive completed items.

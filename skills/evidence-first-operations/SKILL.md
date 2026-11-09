---
name: evidence-first-operations
description: Use when reporting whether operational work is truly done.
version: 1.0.0
license: MIT
author: Henry Harrigan
---

# Evidence-First Operations

## Purpose

Prevent plausible progress from being reported as completion.

## State ladder

Keep these states separate:

1. **Planned**: the intended method exists.
2. **Written**: files or configuration were changed.
3. **Tested**: the changed artifact passed a relevant check.
4. **Deployed**: the artifact reached the target environment.
5. **Read back**: the target system returned the expected persisted state.
6. **Observed**: the requested real-world behavior occurred.

Never use evidence from one state to claim a later state.

## Workflow

1. Translate the request into observable acceptance criteria.
2. Identify the system of record for each criterion.
3. Make the smallest bounded change.
4. Exercise the changed path with a real test.
5. Read the exact destination state after any external write.
6. Preserve identifiers, timestamps, and verification output.
7. Report the highest state actually proven and name any remaining gap.

## Failure language

Use precise phrases:

- `written, not tested`
- `tested locally, not deployed`
- `deployed, readback pending`
- `read back successfully`
- `blocked before mutation`

## Completion gate

Call work complete only when every requested criterion has direct evidence and no unexplained task-owned process, file, tab, or temporary service remains.

---
name: durable-task-handoffs
description: Use when work must survive a chat or agent boundary.
version: 1.0.0
license: MIT
author: Henry Harrigan
---

# Durable Task Handoffs

## Purpose

Make delegated work resumable without relying on conversation memory.

## Required card fields

Every durable task needs:

- Concrete outcome
- Named owner
- Evidence required for completion
- Exact scope and exclusions
- Smallest safe next action
- Dependencies and blockers
- Canonical paths or record identifiers

## Worker contract

1. Read the complete card and linked context.
2. Stay inside the allowlist.
3. Leave checkpoints during long work.
4. Attach commands, files, IDs, and verification receipts.
5. Block rather than invent missing scope.
6. Mark complete only after acceptance evidence exists.

## Orchestrator contract

Verify the board state and artifacts before telling the user delegated work is done. A worker summary is a lead, not proof of an external side effect.

## Blocked-state handoff

Record the blocker, owner of the unblock, exact needed action, preserved paths, and resume command. Close idle task-owned resources after saving that handoff.

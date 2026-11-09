---
name: approval-gated-external-actions
description: Use before sending, publishing, charging, or changing live records.
version: 1.0.0
license: MIT
author: Henry Harrigan
---

# Approval-Gated External Actions

## Purpose

Separate research and preparation from consequential external writes.

## Classify the action

Treat these as commitment points:

- Sending a message or email
- Publishing public content
- Charging, refunding, or changing billing
- Editing calendars, permissions, domains, or live customer records
- Deploying to production

## Workflow

1. Collect current evidence read-only.
2. Resolve the exact destination identity.
3. Prepare the complete proposed payload.
4. Show the user what will happen, where, and to whom.
5. Bind approval to that exact version.
6. Recheck live prerequisites immediately before execution.
7. Perform one bounded mutation.
8. Read the destination back before reporting success.

## Safety rules

- Approval is not proof of execution.
- A successful API response is not proof of persistence.
- Changed source evidence invalidates an earlier approval.
- Never retry an uncertain non-idempotent write automatically.
- If identity, scope, money, timing, or recipient is ambiguous, stop before commitment.

## Result states

Report one of:

- `prepared, awaiting approval`
- `approved, not executed`
- `executed, readback pending`
- `executed and verified`
- `blocked before execution`

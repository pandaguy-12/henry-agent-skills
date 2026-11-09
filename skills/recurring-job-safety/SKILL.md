---
name: recurring-job-safety
description: Use when creating or operating scheduled agent jobs.
version: 1.0.0
license: MIT
author: Henry Harrigan
---

# Recurring Job Safety

## Purpose

Make scheduled automation quiet, bounded, and verifiable.

## Design

1. Use deterministic collection for empty-tick detection.
2. Invoke a model only when new eligible evidence exists.
3. Persist stable source IDs and content hashes.
4. Separate collection, approval, execution, and notification.
5. Add idempotency keys for every durable write.
6. Deliver only state transitions, not repeated summaries.
7. Store a run receipt with status, evidence, and errors.

## Failure rules

- A timeout is unknown state, not automatic failure.
- Never retry an uncertain external write without reconciliation.
- Do not advance watermarks after blind or partial collection.
- A scheduler success only proves the runner finished; inspect semantic output.

## Verification

Run one controlled invocation, inspect its artifact, check scheduler state, confirm the next run, and verify that an empty second run stays quiet.

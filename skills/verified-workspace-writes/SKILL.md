---
name: verified-workspace-writes
description: Use when writing durable files into a shared workspace.
version: 1.0.0
license: MIT
author: Henry Harrigan
---

# Verified Workspace Writes

## Purpose

Protect shared documents from stale overwrites and false success claims.

## Workflow

1. Resolve the canonical destination.
2. Read the complete current file before editing.
3. Preserve formatting, line endings, and concurrent additions.
4. Apply the smallest targeted change.
5. Use optimistic concurrency when the storage system supports versions or hashes.
6. Verify the final bytes through the authoritative read path.
7. Record the destination, version or digest, and unique marker.

## Rules

- Never rebuild a shared file from an old local copy.
- A write acknowledgement is not a readback receipt.
- When cloud placeholders fail locally, use the authenticated provider path before declaring the file unavailable.
- Keep temporary staging files outside the user-facing destination.
- Remove only task-owned staging artifacts after verification.

## Completion evidence

A complete write receipt includes the destination identifier, previous and current version when available, byte count or digest, and confirmation that the intended marker appears exactly once.

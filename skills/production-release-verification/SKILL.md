---
name: production-release-verification
description: Use when proving a release is live in production.
version: 1.0.0
license: MIT
author: Henry Harrigan
---

# Production Release Verification

## Purpose

Distinguish a source change from a verified live release.

## Release gates

1. Record the exact source revision.
2. Build and test that revision.
3. Preserve the current rollback target.
4. Deploy through the canonical release path.
5. Capture the provider's deployment identifier.
6. Probe the immutable deployment URL when available.
7. Probe the stable project URL.
8. Probe the custom production domain.
9. Verify a concrete marker from the released change.
10. Confirm no temporary deploy process remains.

## Reporting

State these independently:

- committed
- CI passed
- deployed
- production read back
- user behavior confirmed

A green pull-request check is not a production deployment. An HTTP success without a change-specific marker is availability evidence, not release evidence.

## Completion receipt

Include source revision, deployment identifier, live URL, status code, marker result, rollback target, and cleanup state.

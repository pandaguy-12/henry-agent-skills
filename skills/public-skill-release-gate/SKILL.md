---
name: public-skill-release-gate
description: Use before publishing a private operating skill publicly.
version: 1.0.0
license: MIT
author: Henry Harrigan
---

# Public Skill Release Gate

## Purpose

Publish proof of work without exposing private operations or republishing material without permission.

## Eligibility

A public skill must have clear ownership or redistribution rights, a generic reusable purpose, and no dependency on private systems or data.

## Review

1. Read the complete source package and support files.
2. Confirm authorship, license, and attribution requirements.
3. Rewrite a public edition instead of copying private operational detail.
4. Remove identities, contact details, credentials, private hosts, account IDs, absolute paths, and proprietary assets.
5. Replace real examples with synthetic examples.
6. Validate every local pointer and included file.
7. Run deterministic secret, privacy, and history scans.
8. Stage locally before any public branch or pull request exists.
9. Commit and push only the exact scanned bytes.
10. Read the public repository back after publication.

## Fail closed

Uncertain license, unresolved identity, scan findings, missing support files, or source drift blocks publication.

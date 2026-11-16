---
name: scoped-browser-operations
description: Use when operating an authenticated web application safely.
version: 1.0.0
license: MIT
author: Henry Harrigan
---

# Scoped Browser Operations

## Purpose

Prevent tab drift, identity mistakes, and accidental live mutations.

## Baseline

Before acting, verify the exact browser profile, account, workspace, URL, object identity, and requested scope.

## Workflow

1. Inspect before mutating.
2. Reacquire the page after every navigation or rerender.
3. Treat selection, typing, saving, publishing, and sending as separate gates.
4. Never infer identity from a display name alone.
5. Stop at password, verification, payment, or consent prompts for human action.
6. After a permitted save, reload and read the exact target value.
7. Close only task-owned tabs and windows.

## Stop conditions

Stop when an action is represented only by an ambiguous icon, a dialog adds unapproved side effects, the target identity cannot be proven, or fresh readback cannot distinguish the intended record.

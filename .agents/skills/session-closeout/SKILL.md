---
name: session-closeout
description: Close a work session in this repository by updating the active continuation doc, archiving history, and keeping active docs clean.
argument-hint: Describe what changed this session and what the next session should do first.
user-invocable: true
---

# Session Closeout

Use this skill at the end of a meaningful work session.

## Goals

- leave one clear next action
- archive stale session history
- keep active docs short and current
- avoid duplicate status across active files

## Closeout Checklist

1. Update `docs/SESSION-CONTINUATION.md` front matter first.
2. Mirror the same state into the top status table.
3. If an active plan is complete, move it to `docs/plans/completed/`.
4. Archive the prior continuation doc into `docs/sessions/` when appropriate.
5. Update `docs/ROADMAP.md` only if milestone state changed.

## Small-Repo Guidance

This repository is tiny. Do not manufacture a large closeout ritual.

A good closeout here usually means:
- one refreshed session continuation file
- one plan archived if it completed
- one short roadmap update if needed

## Done Condition

The next operator should be able to open `docs/SESSION-CONTINUATION.md` and know exactly what to do first.

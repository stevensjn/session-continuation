# Session Continuation Workflow

This document describes how to keep the active session handoff clean for a small React Hello World project.

## Core Principle

The active `docs/SESSION-CONTINUATION.md` file should answer the next-session questions from the first screenful:

1. what branch is active
2. what changed most recently
3. what should happen first next session
4. whether anything is blocked
5. which doc should be loaded next

If those answers require reading the whole file, the continuation doc is too large.

## Start Of Session Procedure

1. Read the YAML front matter in `docs/SESSION-CONTINUATION.md`.
2. Read the top status table.
3. Follow the `Start Here` instruction.
4. Load only the controlling plan, spec, ADR, or troubleshooting doc named there.

## End Of Session Procedure

1. Update `docs/SESSION-CONTINUATION.md` so the next action is explicit.
2. If a plan is complete, move it into `docs/plans/completed/`.
3. Archive the current continuation doc into `docs/sessions/` when ending a significant work session.
4. Create or refresh the next active continuation doc from the template.
5. Update `docs/ROADMAP.md` only if milestone status changed.

## Small-Project Rules

- Keep active docs short.
- Prefer one active plan at a time.
- Avoid creating new categories unless the project actually needs them.
- Archive narrative history instead of leaving it in active docs.

## Why This Matters

A tiny app should not need enterprise ceremony, but it still benefits from fast session recovery. This workflow keeps the routing useful without becoming heavier than the app itself.

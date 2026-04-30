# Plan Composition Guide

This file explains how to route into planning documents without loading unnecessary material.

## Default Load Order

1. `docs/SESSION-CONTINUATION.md`
2. `docs/plans/large-project-brief.md` on `large-project`, otherwise `.agents/skills/session-router/SKILL.md`
3. one active planning document from `docs/plans/`
4. one supporting spec, ADR, pattern, or troubleshooting doc only if required

## Plan Roles

### Brief

Routes a session into the correct deeper document. A brief should stay thin and should not become the tracker.

### Execution Tracker

Tracks the current implementation sequence, blockers, verification expectations, and open slices.

### DDL And Field-Ownership Appendix

Holds durable schema-shaping decisions, field placement rules, and data-model notes that should not be mixed with sprint-by-sprint execution chatter.

### Active Plan

Tracks the next concrete slice of work.

### Completed Plan

Preserves an executed slice without leaving it in active rotation.

## Rules

- keep one active plan as the main tracker when possible
- when the project grows, add a thin brief before the tracker rather than turning the tracker into a session-entry monolith
- keep DDL and field-ownership notes out of the execution tracker unless the task is actually schema-shaping
- archive completed plans into `docs/plans/completed/`
- do not duplicate detailed status across multiple active files
- use a spec for product behavior and an ADR for durable architecture choices

## Large-Project Load Pattern

On `large-project`, use this order:

1. `docs/SESSION-CONTINUATION.md`
2. `docs/plans/large-project-brief.md`
3. `docs/plans/large-project-tracker.md` for active execution work
4. `docs/plans/large-project-ddl-and-field-ownership.md` only for schema, DDL, or field-ownership work

Why it works:

- the brief keeps session-start routing cheap
- the tracker stays focused on active work
- the DDL appendix stays stable and reusable across multiple execution slices

## Current Active Plan Surfaces

- `docs/plans/hello-world-iteration-plan.md`
- `docs/plans/large-project-brief.md`
- `docs/plans/large-project-tracker.md`

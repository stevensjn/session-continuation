---
role: routing-brief
scope: large-project
updated: 2026-04-30
---

# Large Project Brief

This document is the thin router for the `large-project` branch.

Its job is to answer one question quickly: which deeper document should this session load next?

## Why This File Exists

In a larger project, loading the tracker, schema appendix, specs, patterns, and ADRs at session start wastes time and increases drift. The brief keeps the entry path narrow.

## Load Order

Always start with:

1. `docs/SESSION-CONTINUATION.md`
2. this brief

Then choose exactly one primary next document.

## Task Classes

### Active Execution Work

Load:
- `docs/plans/large-project-tracker.md`

Use this for:
- slice sequencing
- blockers
- validation expectations
- current in-flight implementation work

### Schema, DDL, Or Field Ownership

Load:
- `docs/plans/large-project-ddl-and-field-ownership.md`

Use this for:
- schema shape
- field placement
- backend ownership boundaries
- migration-oriented notes

Add the tracker only if current execution sequencing also matters.

### Product Behavior Or UX Contract

Load:
- `docs/specs/hello-world-spec.md`

### Durable Architecture Decision

Load:
- `docs/decisions/ADR-001-react-hello-world-scope.md`

### Implementation Pattern

Load:
- `docs/patterns/react-component-pattern.md`

### Troubleshooting Or Operational Support

Load:
- `docs/troubleshooting/local-dev-runbook.md`

## Stop Rule

Stop loading documents once:

1. the task class is clear
2. one primary deeper document is open
3. no unanswered question requires a second deep document

## Why This Workflow Works

The brief keeps the routing logic separate from the tracker. That separation matters because routing logic changes slowly, while implementation status changes frequently.
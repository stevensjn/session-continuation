# Large Project Workflow Explainer

This document explains the difference between the small-project and large-project workflows in this repository.

## Small-Project Workflow

The small-project version assumes a narrow product surface.

Typical load path:

1. `docs/SESSION-CONTINUATION.md`
2. one active plan or one feature spec
3. work begins

Why it works:

- the number of moving parts is low
- one controlling document is often enough
- the cost of opening an extra doc is small, but usually unnecessary

## Large-Project Workflow

The large-project version assumes a broader product with multiple concurrent concerns.

Typical load path:

1. `docs/SESSION-CONTINUATION.md`
2. `docs/plans/large-project-brief.md`
3. one deeper document chosen by task class

Possible deeper documents:

- `docs/plans/large-project-tracker.md`
- `docs/plans/large-project-ddl-and-field-ownership.md`
- a spec, ADR, pattern doc, or troubleshooting runbook

Why it works:

- the brief prevents default overloading of every session
- the tracker stays operational instead of becoming a giant reference dump
- the DDL appendix keeps durable model guidance stable across multiple execution slices

## Core Difference

The small workflow optimizes for simplicity. The large workflow optimizes for selectivity.

That difference matters because a large project fails when every session starts by reopening all deep docs. The branch split in this repository makes that tradeoff visible.
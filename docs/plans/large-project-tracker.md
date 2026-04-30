# Large Project Tracker

Status: Active

## Purpose

This tracker represents the active execution surface for a hypothetical large React-led product. It is the document to load when the task is about current sequencing, blockers, validation, or in-flight implementation slices.

## Imagined Product Shape

The large-project branch assumes a broader application than the Hello World baseline, including:

- multiple React feature areas
- backend APIs
- permission-sensitive routes
- shared UI patterns
- a data model large enough to justify separated schema guidance

## Current Example Workstreams

### Workstream 1: App Shell And Navigation

Status: In progress

Focus:
- document top-level route grouping
- define the session-entry path for UI tasks
- keep the navigation pattern aligned with the routing brief

### Workstream 2: Feature Delivery Tracking

Status: In progress

Focus:
- show how a tracker can hold active slices without becoming a schema appendix
- keep validation expectations near the active work

### Workstream 3: Data Model Boundaries

Status: Routed to appendix

Focus:
- do not expand this tracker with table-shape detail
- defer schema ownership and DDL notes to `docs/plans/large-project-ddl-and-field-ownership.md`

## Example Next Slices

1. Define one module-level execution slice for frontend work.
2. Define one backend-adjacent slice that depends on route permissions.
3. Define one schema-touching slice and route it into the DDL appendix before implementation.

## Validation Pattern

For a larger project, validate in layers:

- document routing first
- then the slice-level plan
- then the implementation or schema surface

This keeps active execution decisions near the work without dragging every reference doc into each session.
# ADR-001: Keep The React App Intentionally Minimal

- Status: Accepted
- Decision Date: 2026-04-30

## Context

This repository exists primarily to demonstrate session routing and documentation structure. The underlying application is only a simple React Hello World example.

Without a clear decision, future sessions might gradually add unnecessary architecture, multiple workstreams, or documentation overhead that exceeds the size of the app.

## Decision

The example application will remain intentionally minimal:

- one simple React application
- one primary greeting screen
- only a few optional follow-up enhancements
- documentation should remain proportionate to that size

## Rationale

A tiny app is the best surface for demonstrating how routing discipline works. The point is not to simulate a large enterprise platform. The point is to show how a small project can still preserve continuity between sessions.

## Consequences

Positive:
- easier session recovery
- lower documentation overhead
- clearer routing examples

Negative:
- some workflow examples will stay illustrative rather than exercised by complex code
- the project intentionally stops short of demonstrating large-scale architecture

## Related Documents

- `docs/SESSION-CONTINUATION.md`
- `docs/plans/hello-world-iteration-plan.md`
- `docs/specs/hello-world-spec.md`

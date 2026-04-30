---
name: session-router
description: Route work in this repository by deciding which small set of documents to load for a React Hello World session.
argument-hint: Describe the task or session goal that needs routing.
user-invocable: true
---

# Session Router

Use this skill to keep session start lightweight, even when the project itself is large.

## What This Skill Does

It decides:

1. which document to load first after the session continuation file
2. which documents are unnecessary for the current task
3. when enough context has been loaded to begin work

## Always Load First

1. `docs/SESSION-CONTINUATION.md`
2. `docs/plans/large-project-brief.md` on `large-project`, otherwise `docs/plans/README.md` only if the next document role is still unclear
3. this skill when routing is needed

## Task Classes

Choose one controlling task class:

- session housekeeping
- product behavior refinement
- implementation shape discussion
- execution tracking for a large workstream
- schema, DDL, or field-ownership work
- durable architecture decision
- troubleshooting or operator support
- documentation consistency audit

## Routing Rules

### Session Housekeeping

Load:
- `docs/session-workflow.md`

### Product Behavior Refinement

Load:
- `docs/specs/hello-world-spec.md`
- `docs/plans/hello-world-iteration-plan.md` if execution sequencing matters

### Implementation Shape Discussion

Load:
- `docs/patterns/react-component-pattern.md`
- `docs/plans/hello-world-iteration-plan.md` if active work tracking matters

### Execution Tracking For A Large Workstream

Load:
- `docs/plans/large-project-brief.md`
- `docs/plans/large-project-tracker.md`

Do not load the DDL appendix unless the task actually changes schema or field ownership.

### Schema, DDL, Or Field-Ownership Work

Load:
- `docs/plans/large-project-brief.md`
- `docs/plans/large-project-ddl-and-field-ownership.md`

Add `docs/plans/large-project-tracker.md` only if rollout order or active slice tracking also matters.

### Durable Architecture Decision

Load:
- `docs/decisions/ADR-001-react-hello-world-scope.md`

### Troubleshooting Or Operator Support

Load:
- `docs/troubleshooting/local-dev-runbook.md`

### Documentation Consistency Audit

Load:
- `.agents/skills/documentation-drift-audit/SKILL.md`
- `docs/README.md`
- `docs/SESSION-CONTINUATION.md`

## Stop Rule

Begin work once:

1. the task class is clear
2. one controlling document is loaded
3. no unresolved question requires another deeper doc

Do not keep reading for reassurance.

## Output Expectation

After routing, be able to state:

- task class
- docs loaded
- docs deferred
- why current context is sufficient

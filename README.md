# Session Continuation

This repository is a documentation-first example project that shows how to run AI-assisted work sessions for a React application at two different scales.

It intentionally contains no production code. The goal is to demonstrate:

- scan-first session handoff
- small-document routing discipline on `main`
- scaled routing discipline on `large-project`
- clear documentation categories under `docs/`
- reusable skills for session start, session closeout, and documentation drift checks

## Project Shape

The repository teaches two variants of the same idea:

- `main` shows the smallest useful workflow for a simple React Hello World application
- `large-project` shows how the workflow changes when the imagined React project grows into a multi-workstream product with active execution tracking and schema ownership concerns

On the `large-project` branch, the imagined application becomes a much broader React platform with multiple modules, backend APIs, permission-sensitive routes, and data-model work that cannot live in one overloaded plan file.

## Branch Guide

### `main`

Use `main` when you want the simplest possible session-routing example:

- one session continuation file
- one active plan
- optional spec, ADR, pattern, or troubleshooting doc

This branch works because the project is small enough that one controlling document can usually answer the next-session question.

### `large-project`

Use `large-project` when you want a scaled workflow closer to a real product team:

- one scan-first session continuation file
- one thin plan brief that routes the task
- one execution tracker for sequencing, blockers, and validation
- one separated DDL and field-ownership appendix for schema-shaping work

This branch works because it keeps each document focused on one job. The session continuation file answers "what next," the brief answers "which deeper doc," the tracker answers "what is active," and the DDL appendix answers "how the data model is shaped."

## Why The Large-Project Workflow Works

The larger the project gets, the more expensive it becomes to load everything at session start. A thin brief plus separated tracker and DDL appendix works for three reasons:

1. it reduces context sprawl by keeping deep docs out of the default load path
2. it prevents execution chatter from polluting durable schema and field-ownership guidance
3. it lowers documentation drift by giving every active file a single purpose

## Start Here

At the start of a new work session, load these in order:

1. `docs/SESSION-CONTINUATION.md`
2. `.agents/skills/session-router/SKILL.md`
3. the controlling document named in the session continuation file

On `large-project`, that controlling document will usually be `docs/plans/large-project-brief.md` rather than the execution tracker directly.

## Repository Intent

This repo exists as a teaching and scaffolding example. It demonstrates both ends of the workflow spectrum: the small-project version that stays intentionally lean, and the large-project version that adds just enough routing structure to keep a bigger codebase understandable.

## Key Principles

- Keep the current session state in one place.
- Load the minimum number of docs needed to begin work.
- Separate plans, specs, patterns, ADRs, and archived sessions.
- Prefer short active docs and deeper appendices only when needed.

## Important Directories

- `docs/` stores all project documentation.
- `.agents/skills/` stores repo-local workflow skills.
- `.github/copilot-instructions.md` stores always-on repository guidance.

## Suggested Next Exercise

If you want to extend this example later, either:

- add a small `src/` folder and keep using the `main` workflow, or
- expand the `large-project` branch docs into a full-stack example with frontend, backend, and schema reference surfaces

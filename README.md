# Session Continuation

This repository is a documentation-first example project that shows how to run AI-assisted work sessions for a simple React Hello World application.

It intentionally contains no production code. The goal is to demonstrate:

- scan-first session handoff
- small-document routing discipline
- clear documentation categories under `docs/`
- reusable skills for session start, session closeout, and documentation drift checks

## Project Shape

The imagined application is a small React app with one screen:

- a page that renders `Hello, world!`
- a tiny amount of state for display options
- a minimal future roadmap for adding one or two small UI enhancements

## Start Here

At the start of a new work session, load these in order:

1. `docs/SESSION-CONTINUATION.md`
2. `.agents/skills/session-router/SKILL.md`
3. the controlling document named in the session continuation file

## Repository Intent

This repo exists as a teaching and scaffolding example. It demonstrates how a session-routing system can stay lightweight for a tiny application rather than inheriting the complexity of a much larger product.

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

If you want to extend this example later, add a small `src/` folder with a React component and then update the session docs so they reference a concrete implementation surface.

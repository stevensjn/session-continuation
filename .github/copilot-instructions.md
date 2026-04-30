# Copilot Instructions

This repository demonstrates a documentation-first workflow for a simple React Hello World application.

## Session Start Rule

Always load `docs/SESSION-CONTINUATION.md` first.

If routing is still unclear after that, load `.agents/skills/session-router/SKILL.md`.

## Project Scope

The application is intentionally small:

- one React page
- one visible greeting
- optional future enhancements such as theme toggle or language toggle

Keep all documentation proportional to that scope.

## Documentation Policy

- All project documentation belongs under `docs/`.
- Keep active docs short and actionable.
- Put historical material in `docs/sessions/` or `docs/plans/completed/`.
- Do not duplicate the same status in multiple active documents.

## Workflow Expectations

During a normal session:

1. Read the session continuation header and `Start Here` block.
2. Load one controlling plan, spec, or ADR only if the session doc points to it.
3. Begin work once the task class and controlling document are clear.

## Verification Expectations

For this documentation-only example repository:

- verify links and document structure
- keep cross-references accurate
- prefer simple git validation over heavyweight build steps

## Editing Standards

- Use ASCII unless a file already needs something else.
- Preserve the role of each documentation folder.
- Rewrite shared workflow ideas so they fit a small React sample app instead of a large enterprise system.

## Skills In This Repo

The repo ships with three lightweight skills:

- session-router
- session-closeout
- documentation-drift-audit

Use them as guidance for how a smaller project can still benefit from explicit workflow automation.

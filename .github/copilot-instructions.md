# Copilot Instructions

This repository demonstrates documentation-first workflow patterns for both a tiny React Hello World app and a much larger React-led product.

## Session Start Rule

Always load `docs/SESSION-CONTINUATION.md` first.

If routing is still unclear after that, load `.agents/skills/session-router/SKILL.md`.

## Project Scope

The repository has two operating modes:

- `main` is intentionally small
- `large-project` demonstrates a scaled workflow with a routing brief, an execution tracker, and a separated DDL appendix

Keep the documentation proportional to the selected branch.

## Documentation Policy

- All project documentation belongs under `docs/`.
- Keep active docs short and actionable.
- Put historical material in `docs/sessions/` or `docs/plans/completed/`.
- Do not duplicate the same status in multiple active documents.

## Workflow Expectations

During a normal session:

1. Read the session continuation header and `Start Here` block.
2. On `large-project`, load the routing brief before opening deeper planning docs.
3. Load one controlling plan, spec, ADR, or appendix only if the session doc or brief points to it.
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

Use them as guidance for how both a smaller and larger project can benefit from explicit workflow automation without loading every document by default.

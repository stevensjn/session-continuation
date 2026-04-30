# Session Continuation Agent Entry Point

This repository demonstrates two documentation-routing workflows for a React application:

- a minimal `main` branch for a tiny Hello World app
- a `large-project` branch for a much broader product with multiple active documentation layers

## Start Here

1. Load `docs/SESSION-CONTINUATION.md` for the current branch, active workstream, and next action.
2. Load `.github/copilot-instructions.md` for always-on repo policy.
3. Use the workflow skill that matches the task from `.agents/skills/`.

## Canonical Workflow Skills

### Session Router

- Skill path: `.agents/skills/session-router/SKILL.md`
- Use when: starting a session, switching tasks, or deciding which doc to load next.

### Session Closeout

- Skill path: `.agents/skills/session-closeout/SKILL.md`
- Use when: ending a session, archiving the current continuation doc, and preparing the next one.

### Documentation Drift Audit

- Skill path: `.agents/skills/documentation-drift-audit/SKILL.md`
- Use when: checking whether the README, roadmap, session doc, and plans still agree.

## Source Of Truth Order

1. `docs/SESSION-CONTINUATION.md`
2. `docs/plans/large-project-brief.md` on `large-project`, otherwise `docs/plans/README.md`
3. the active tracker, spec, ADR, or appendix for the current task
4. `.github/copilot-instructions.md`
5. archived material under `docs/sessions/` and `docs/plans/completed/`

## Scope Reminder

Choose the workflow that matches the branch:

- on `main`, do not invent enterprise process where a short document will do
- on `large-project`, use the brief and split-plan model to prevent large-project context sprawl

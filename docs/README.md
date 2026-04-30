# Documentation Structure

All project documentation lives under `docs/`.

This repository is intentionally tiny, but the documentation layout still separates concerns so an operator or agent can recover context quickly.

## Directory Layout

```text
docs/
├── README.md
├── ROADMAP.md
├── SESSION-CONTINUATION.md
├── session-workflow.md
├── decisions/
├── other/
├── patterns/
├── plans/
│   └── completed/
├── sessions/
├── specs/
├── templates/
└── troubleshooting/
```

## Folder Roles

| Folder | Purpose | Example In This Repo |
|---|---|---|
| `docs/` root | Current high-level operating docs | session continuation and roadmap |
| `decisions/` | Architecture decisions | why React stays minimal |
| `other/` | Temporary or exploratory notes | brainstorming notes |
| `patterns/` | Reusable implementation patterns | a simple component pattern |
| `plans/` | Active implementation plans | greeting enhancement plan |
| `plans/completed/` | Archived executed plans | completed initial scaffold plan |
| `sessions/` | Archived session continuation docs | a previous session handoff |
| `specs/` | Feature or UX specifications | hello-world feature spec |
| `templates/` | Reusable doc templates | session continuation template |
| `troubleshooting/` | Runbooks and incident notes | local dev troubleshooting guide |

## Load Discipline

Default load order for a new session:

1. `docs/SESSION-CONTINUATION.md`
2. `.agents/skills/session-router/SKILL.md`
3. one controlling doc from `plans/`, `specs/`, or `decisions/`

Do not load everything just because it exists.

## Small Vs Large Workflow

On `main`, the controlling doc is usually one active plan or one feature spec.

On `large-project`, the recommended path is:

1. `docs/SESSION-CONTINUATION.md`
2. `docs/plans/large-project-brief.md`
3. `docs/plans/large-project-tracker.md` for active execution work
4. `docs/plans/large-project-ddl-and-field-ownership.md` only when schema, DDL, or field ownership questions are in scope

This works because the brief stays thin, the tracker stays operational, and the DDL appendix stays durable.

## Why This Structure Exists

Even for a Hello World app, the difference between active docs, archived docs, and permanent decisions matters. A small project becomes easier to maintain when each file has one clear role.

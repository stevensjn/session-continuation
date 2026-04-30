---
name: documentation-drift-audit
description: Check whether the active docs in this repository still agree on current state, next action, and load order.
argument-hint: Describe the suspected documentation drift or the files you want compared.
user-invocable: true
---

# Documentation Drift Audit

Use this skill when the documentation may have started to disagree with itself.

## Compare These Sources

1. `docs/SESSION-CONTINUATION.md`
2. `docs/ROADMAP.md`
3. `docs/plans/README.md`
4. the active plan under `docs/plans/`
5. `README.md`

## What To Check

- does the session continuation file point to the correct next doc
- does the roadmap still describe the right current phase
- does the active plan match the workstream named in the session doc
- does the README describe the same repository purpose as the active docs

## Output Format

State:

- findings, ordered by severity
- any open questions
- the minimum set of files that need updating

## Stop Rule

Do not open archived sessions or completed plans unless the active docs cannot explain the mismatch.

# Local Development Troubleshooting Runbook

This runbook exists for the day the documentation-only example grows into an actual React app.

## Common Problems

### Problem: The greeting does not appear

Checks:
- confirm the app entry point renders the `App` component
- confirm the greeting component returns visible text
- confirm the browser console shows no fatal runtime error

### Problem: A session points to the wrong controlling document

Checks:
- compare `docs/SESSION-CONTINUATION.md` with `docs/plans/README.md`
- ensure the `next_doc` field matches the active workstream
- archive stale plans rather than leaving them active

## Why This File Matters

Troubleshooting docs are useful only when they stay operational. Keep this file concrete and update it only when a real recurring problem appears.

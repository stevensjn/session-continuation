# React Component Pattern

This pattern document shows what a tiny component structure might look like if the Hello World app later receives implementation files.

## Pattern Goal

Keep the component model boring and obvious.

## Suggested Structure

- `App` owns the page shell
- `HelloMessage` renders the greeting
- optional local state in `App` controls a tiny display preference

## Pattern Rules

- avoid global state until the app genuinely needs it
- keep props explicit
- keep components small enough to understand at a glance
- prefer readability over abstraction

## Routing Use

A future session should load this document only when the task is about implementation shape or component structure. It should not be a default session-entry document.

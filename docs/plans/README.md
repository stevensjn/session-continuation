# Plan Composition Guide

This file explains how to route into planning documents without loading unnecessary material.

## Default Load Order

1. `docs/SESSION-CONTINUATION.md`
2. `.agents/skills/session-router/SKILL.md`
3. one active plan from `docs/plans/`
4. one supporting spec, ADR, pattern, or troubleshooting doc only if required

## Plan Roles

### Active Plan

Tracks the next concrete slice of work.

### Completed Plan

Preserves an executed slice without leaving it in active rotation.

## Rules

- keep one active plan as the main tracker when possible
- archive completed plans into `docs/plans/completed/`
- do not duplicate detailed status across multiple active files
- use a spec for product behavior and an ADR for durable architecture choices

## Current Active Plan

- `docs/plans/hello-world-iteration-plan.md`

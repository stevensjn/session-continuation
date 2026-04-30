# Architecture Decision Records

This directory stores the durable technical decisions for the Hello World example project.

## Purpose

ADRs capture choices that should stay stable across multiple sessions. For a small React example, these decisions should remain rare and high signal.

## When To Create An ADR

Create an ADR when a decision affects future structure, such as:

- whether the app remains a single page
- whether state stays local or moves to a global store
- whether styling remains CSS-based or adopts another approach

## When Not To Create An ADR

Do not create an ADR for ordinary session tasks, tiny text changes, or experimentation that has not become a durable decision.

## Current ADRs

- `ADR-001-react-hello-world-scope.md`

## Format

A useful ADR for this repo should include:

- status
- context
- decision
- rationale
- consequences
- related documents

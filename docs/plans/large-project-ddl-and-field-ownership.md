# Large Project DDL And Field Ownership

Status: Reference Appendix

## Purpose

This appendix exists to demonstrate why larger projects often split schema-shaping content away from the execution tracker.

## What Belongs Here

- DDL examples
- field placement rules
- ownership boundaries between modules
- migration notes
- durable model-shape constraints

## What Does Not Belong Here

- sprint-by-sprint progress notes
- temporary blockers unrelated to schema
- daily execution sequencing

## Example Ownership Model

For a larger React plus API platform, a stable ownership split might look like this:

- UI presentation rules live in pattern docs
- feature behavior lives in specs
- active sequencing lives in the tracker
- field ownership and DDL notes live here

## Example DDL Fragment

```sql
create table feature_modules (
  id integer primary key,
  key varchar(100) not null unique,
  display_name varchar(200) not null,
  deleted bit not null default 0
);

create table feature_routes (
  id integer primary key,
  module_id integer not null,
  route_key varchar(150) not null unique,
  path varchar(255) not null,
  foreign key (module_id) references feature_modules(id)
);
```

## Why The Split Works

Execution trackers change often. DDL guidance should change only when the model itself changes. Keeping them apart prevents two common failures:

1. the tracker becomes unreadable because it absorbs too much durable reference material
2. schema notes become unreliable because they are buried inside a fast-moving task log

## Escalation Rule

Only load this appendix by default when the task changes schema, field ownership, or migration behavior. Otherwise, stay in the tracker or spec layer.
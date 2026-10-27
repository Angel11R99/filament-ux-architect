# Existing module refactoring checklist

Use this checklist to find workflow friction before changing architecture. Do not change an effective interface just to make it look different.

## Inspect and understand

- [ ] Identify installed Filament major version, plugins, panel configuration, and local conventions.
- [ ] Inspect Resource, Pages, Schemas, Tables, Actions, Widgets, Relation Managers, policies, models, relationships, and relevant tests.
- [ ] Describe the actor, entry point, frequent task, outcome, data already available, and permission boundaries.

## Diagnose

- [ ] Find oversized forms, cramped modals, unnecessary slide-overs, and workflows missing context.
- [ ] Find overloaded tables, missing or duplicate filters, permanent low-value columns, and horizontal scrolling.
- [ ] Find redundant fields, navigation, tabs, actions, or repeated information.
- [ ] Check empty states, status meaning, discoverability, validation, mobile behavior, and keyboard interaction.
- [ ] Check query loading, pagination, N+1 risks, tenant scope, and direct action authorization.
- [ ] Decide whether widgets or alternative presentations add actual value.

## Choose and implement

- [ ] Compare at least two viable architectures for a material refactor.
- [ ] Choose the strongest option with the least unnecessary complexity and explain the reason.
- [ ] Preserve business logic, schema, permissions, routes, validation, relationships, and public contracts unless change is authorized.
- [ ] Verify exact APIs and third-party capabilities for the installed versions.
- [ ] Avoid unrelated module changes and unnecessary dependencies.

## Validate and report

- [ ] Check create, view, edit, action, and relationship flows affected by the change.
- [ ] Check unauthorized access and server-side enforcement, including direct access where relevant.
- [ ] Check error, empty, and validation states plus keyboard and responsive behavior.
- [ ] Run relevant tests and project-required formatting or static checks.
- [ ] Report decisions, files changed, verification, and remaining limitations.

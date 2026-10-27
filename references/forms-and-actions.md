# Forms and actions

Use field semantics, workflow length, and impact to shape data entry. Verify the installed version's Schema, Form, Action, and relationship APIs.

## Form organization

- Group fields by the user's task and information hierarchy. Use sections or grids when they improve scanning; keep optional detail secondary.
- Choose text, textarea, select, searchable select, date/time, toggle, checkbox, radio, repeater, builder, upload, editor, or relationship-aware inputs based on data semantics and scale.
- Use reactive and conditional fields only where they prevent irrelevant choices or explain dependencies. Keep state transitions understandable.
- Avoid duplicate entry when context or relationships already provide the information. Preserve validation and business rules.
- Use helper text for decisions users cannot infer from a label. Make validation errors specific and accessible.
- Keep long or relationship-heavy editing on a page with adequate space.

## Action sizing

- **Modal:** brief, bounded actions with a small number of inputs.
- **Slide-over:** contextual medium tasks where the underlying record or list remains useful.
- **Dedicated page:** extensive editing, rich relationship management, substantial review, or multi-stage processes.
- **Wizard:** sequential data capture where prior answers affect later steps; communicate progress and persistence behavior.

These are starting points. Verify that the chosen interaction is supported by the installed version and does not create excessive scrolling or lost context.

## Mutation safety

- Separate primary and secondary actions; use consistent placement and clear labels.
- Explain impact before destructive or sensitive actions; require confirmation or reason where business rules call for it.
- Apply policies and validation on the server, including row, page, bulk, and direct action paths.
- Use notifications to report the outcome and next step without leaking sensitive data.
- Preserve audit history and transaction semantics required by the application.

# Component selection

Use this guide to select an interface around user work. Confirm exact APIs in documentation for the installed Filament major version.

## Questions to answer

- Who uses the module, what are their frequent tasks, and how do they reach it?
- How many records are managed, how complex are they, and what must users compare?
- What information is read-only, editable, sensitive, or time-critical?
- Which related records need their own search, lifecycle, or actions?
- Which actions are frequent, destructive, approval-gated, or space-intensive?
- What context must remain visible while the user acts?
- What keyboard, mobile, authorization, tenant, performance, and localization requirements apply?

## Interaction decision guide

| Need | Consider | Fit and limits |
|---|---|---|
| Scan, compare, sort, filter, or process records in volume | Table | Keep a focused default column set; make less common data available without requiring permanent width. |
| A few fields for one short task | Modal action | Good for quick, bounded work. Do not place extensive forms or several dependent relationships in a cramped modal. |
| Medium task while retaining list context | Slide-over action | Useful for contextual review or edits. Verify support and ensure content does not become a long scrolling page. |
| Extensive record editing, multiple relationships, or rich workflow | Dedicated resource page or custom page | Gives room for structure and validation; make navigation and save/cancel paths clear. |
| Required sequence with meaningful dependencies | Wizard | Use only when step order supports the task; avoid splitting unrelated fields into artificial steps. |
| Read-only record review | Infolist | Present information as information, not disabled inputs. |
| Related records managed independently | Relation Manager or linked page | Choose based on interaction density, lifecycle, and need for independent navigation. |
| Summary metric or trend | Widget | Add only when it supports a decision or action; keep definitions and time ranges clear. |
| Custom operational workflow not expressed well by standard resource pages | Custom page / supported extension | Validate maintenance cost, authorization, accessibility, and version-specific APIs. |

## Evaluate alternatives

For nontrivial architecture, compare at least two credible options against task time, context retention, information density, error risk, discoverability, responsive behavior, and implementation complexity. Choose the least complex fit. A visually impressive component is not evidence of a better workflow.

## Layout and field choices

Use sections, grids, fieldsets, flex layouts, tabs, collapsible sections, and split layouts only after confirming they exist in the installed version and improve grouping or scanning. Choose inputs by data semantics and user expectations: text, select, searchable relationship, date/time, boolean, repeated structured data, file, rich text, or conditional field. Make dependent values and validation understandable, and avoid asking for data already available from context.

## Safety and inclusion

Make destructive intent explicit and provide confirmation appropriate to impact. Do not rely on hidden buttons or navigation visibility as authorization. Ensure labels, focus order, validation feedback, contrast, and keyboard operation. Verify access for direct URLs and server actions as well as the visible interface.

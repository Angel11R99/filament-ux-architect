# Module architecture patterns

Patterns are starting points. Adapt them to observed workflows and installed capabilities; do not force every module into a template.

## Operational management

- **Use for:** High-frequency processing of many records and status changes.
- **Structure:** Focused table, useful search and filters, clear status, prioritized row actions, optional meaningful summary.
- **Navigation:** One discoverable resource entry, grouped with related operational areas.
- **Actions:** Make the common next step prominent; keep rare or destructive actions contextual and protected.
- **Mistakes:** Too many columns, duplicate filters, unsafe bulk changes, action overload.
- **Responsive / alternatives:** Keep core identifiers and status usable at narrow widths; consider a purpose-built work queue or custom record view when rows cannot express the task.

## Scheduling and calendar-oriented

- **Use for:** Time-based allocation, availability, and conflict management.
- **Structure:** Use a verified calendar integration or a date/time filtered table when the calendar is not available or useful. Keep record detail and conflict handling clear.
- **Navigation:** Make date ranges and resource scope easy to understand.
- **Actions:** Create, reschedule, cancel, and inspect conflicts with confirmation proportional to impact.
- **Mistakes:** Treating a calendar plugin's event as the business record, hiding availability rules, or assuming concurrency safety from the UI.
- **Responsive / alternatives:** Provide a list or agenda view where a calendar is hard to use; verify integration callbacks, persistence, permissions, and conflict behavior.

## Financial management

- **Use for:** Charges, invoices, payments, reconciliation, or refunds.
- **Structure:** Tables for transaction review, clear totals and status, dedicated pages for complex accounting or adjustments.
- **Navigation:** Separate operational tasks from configuration and reporting where users need distinct mental models.
- **Actions:** Make amount, currency, affected record, and irreversible effects clear; protect refunds and write-offs.
- **Mistakes:** Ambiguous totals, conflated states, hidden audit context, unsafe bulk operations.
- **Responsive / alternatives:** Preserve amount and status visibility; use detail pages or infolists for audit trails.

## Clinical or patient-record systems

- **Use for:** Sensitive records with distinct administrative and clinical tasks.
- **Structure:** Separate operational lists from detailed record review; use contextual pages, infolists, and independently managed related records where appropriate.
- **Navigation:** Follow user roles and avoid exposing sensitive concepts through unnecessary menu entries.
- **Actions:** Respect policies, assignment, consent, and audit requirements established by the application.
- **Mistakes:** Re-entering existing identity data, conflating administrative and clinical records, exposing sensitive data in tables or notifications.
- **Responsive / alternatives:** Keep critical context and warnings accessible. Do not invent clinical or regulatory rules; preserve domain meaning and seek qualified product owners for domain decisions.

## Inventory and resource tracking

- **Use for:** Items, stock, assets, locations, or reservations.
- **Structure:** Scannable table with availability/state filters; detail page or relation management for movements and history.
- **Navigation:** Group by operational resource and task, not by database table alone.
- **Actions:** Make adjustment reasons and affected quantities explicit; protect irreversible movements.
- **Mistakes:** Showing a mutable current balance without movement context, mixing catalog configuration with stock operations.
- **Responsive / alternatives:** Prioritize identifiers and quantities; use a movement ledger or dedicated workflow for frequent adjustments.

## Configuration and settings

- **Use for:** Low-frequency, high-impact system behavior.
- **Structure:** Group related options on a settings page or small number of pages; explain scope and consequences.
- **Navigation:** Keep settings discoverable but separate from daily operations.
- **Actions:** Save and reset behavior should be explicit; protect secrets and sensitive integrations.
- **Mistakes:** Giant undifferentiated forms, unclear defaults, settings that silently affect unrelated areas.
- **Responsive / alternatives:** Use progressive disclosure for advanced settings; use dedicated pages for complex integrations.

## Reporting and analytics

- **Use for:** Understanding trends, distributions, and operational outcomes.
- **Structure:** Start with user questions, definitions, time range, and filters; add charts only where visual comparison helps.
- **Navigation:** Separate analytical exploration from the operational record workflow when their needs differ.
- **Actions:** Offer a path from aggregate to authorized detail where useful.
- **Mistakes:** Decorative charts, unclear denominators, mixing time ranges, promising real-time data without support.
- **Responsive / alternatives:** Provide accessible labels or tabular summaries; use filtered tables for precise lookup.

## Document management

- **Use for:** Upload, classification, retrieval, review, or lifecycle management.
- **Structure:** Searchable table or list with clear type, owner/context, status, and dates; detail view for metadata and history.
- **Navigation:** Surface documents within their owning workflow when context matters.
- **Actions:** Clarify upload constraints, visibility, replacement, and deletion behavior.
- **Mistakes:** Exposing private storage URLs, ambiguous versions, file actions without authorization checks.
- **Responsive / alternatives:** Use a dedicated page for complex preview/review; verify storage and preview support in the project.

## Approval and multi-step workflows

- **Use for:** Decisions requiring stages, reviewer context, and state transitions.
- **Structure:** Queue grouped by actionable state, detail view with evidence and history, explicit next step.
- **Navigation:** Make pending work easy to find for each responsible role.
- **Actions:** Show consequences and require a reason when the business process needs one.
- **Mistakes:** Treating a wizard as an approval workflow, hiding current state, allowing unauthorized transitions.
- **Responsive / alternatives:** A dedicated page is often clearer than a modal; use a wizard only for guided data entry with real sequence.

## Relationship-heavy master-detail

- **Use for:** A parent record with related records that have independent lifecycles.
- **Structure:** Parent summary plus focused Relation Managers or linked pages; avoid loading every child record into a giant form.
- **Navigation:** Preserve parent context and indicate child counts or states when useful.
- **Actions:** Put child creation and management near the relationship; authorize each operation.
- **Mistakes:** Duplicate parent fields, unbounded nested data, mixing unrelated child types.
- **Responsive / alternatives:** Use separate pages for dense child workflows; use a small repeater only for bounded embedded values.

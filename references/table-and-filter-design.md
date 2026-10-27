# Table and filter design

Design the list around decisions users make while scanning records. Verify every column, filter, summary, and layout API in the installed Filament documentation.

## Columns

- Keep the default set to the identifiers and attributes needed for the primary task. Common starting point: a few key columns plus row actions, adjusted for the domain.
- Select supported text, icon, image, badge, and other column types based on meaning, not decoration.
- Make secondary columns selectable when supported and keep important content available in record detail.
- Use search and sorting only where they match user expectations and can be implemented efficiently.
- Handle long text with a concise representation and a discoverable full view; do not truncate critical data without an alternative.
- Check relationship access for N+1 queries and eager load intentionally.

## Filters

- Add filters for real ways users segment work: state, owner, date, category, or relationship as applicable.
- Avoid duplicate controls for the same condition. Use clear labels, sensible defaults, active filter indicators, and an easy clear path.
- Use date ranges or query filters when the workflow needs them and supported APIs make them maintainable.
- Keep filter queries bounded and authorized. Avoid loading huge option sets into a select.

## Actions and density

- Put the primary frequent action where it is easy to discover. Keep infrequent and destructive actions contextual, labeled, and protected.
- Add bulk actions only when batch semantics are safe and meaningful for each selected record.
- Use grouping, summaries, pagination, and custom record layouts only where they clarify work or comparisons.
- Ensure the table remains useful on narrow screens. Reduce or configure columns and offer a detail path; never use hidden overflow as the sole mobile strategy.

## Empty, loading, and error states

Explain why a list is empty and provide an authorized next action when useful. Distinguish no records from no matching records. Keep loading behavior and query cost appropriate to dataset size.

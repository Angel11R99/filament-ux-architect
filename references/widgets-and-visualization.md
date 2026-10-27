# Widgets and visualization

Widgets should answer a real operational or analytical question. Confirm the native component or installed integration and its API before recommending it.

## Choose the presentation

- **Stats:** Use for a small number of meaningful, scoped KPIs that support a decision. Define scope and time period.
- **Charts:** Use for trends, distributions, or comparisons where shape conveys more than a number. Label axes, units, periods, and filters clearly.
- **Table widgets:** Use for a compact actionable subset, such as recent or pending records, with a clear path to the full list.
- **Custom widgets:** Use when a distinct workflow or visualization is not served adequately by supported native widgets. Keep authorization, query cost, responsive behavior, and accessibility in scope.
- **Timelines and calendars:** Treat as integrations or custom capabilities unless installed Filament or project packages verify native support.

## Dashboard composition

- Organize around user decisions and urgency, not the number of available widgets.
- Avoid duplicate metrics, decorative charts, excessive cards, and dashboards that substitute for a well-designed work queue.
- Keep date ranges and refresh behavior explicit. Do not imply real-time data unless the implementation supports it.
- Provide a textual or tabular route to important insight when chart interaction or color alone would exclude users.

## Performance and access

Scope every query and honor policies and tenant constraints. Avoid loading full datasets for aggregates or chart series; use appropriate aggregates, bounds, and caching only when freshness semantics are clear. Ensure widget visibility is not the only authorization boundary.

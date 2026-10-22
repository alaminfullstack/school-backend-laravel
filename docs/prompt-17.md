# Prompt 17 — Reporting, exports, certificates, and document access

**Mode:** Plan, approve, implement. Split high-volume export jobs into a separate task if necessary.

> Implement a reporting framework and the first approved operational reports: student register/class list, attendance summary, examination/result sheet, fee statement/collection summary, and staff directory as authorized. Include school/session/class/date filters, server-side pagination where appropriate, and export to CSV/Excel/PDF only using packages already installed or explicitly approved.
>
> Reports must respect identical permissions and tenant scoping to normal API endpoints. For large exports, queue generation and provide an authorized, expiring download link; store generated documents privately and clean up expired files. Do not expose public predictable paths. Escape spreadsheet cells that could be interpreted as formulas. For certificates, support institution branding, unique verification/reference numbers if approved, and historical record integrity.
>
> Add tests for authorization, filters, empty/large datasets, escaping, export permissions, temporary link expiry where testable, and tenant isolation. Document which reports are synchronous versus queued and any limits.

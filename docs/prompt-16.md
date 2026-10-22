# Prompt 16 — Dashboard and summary APIs

**Mode:** Plan, approve, implement.

> Build role-specific dashboard APIs for the school ERP. Provide separate, permission-aware summaries for school owner/principal, administrator, teacher, accountant, guardian, and student. Examples may include active enrollment counts, today's attendance, upcoming exams, pending admission reviews, fee collection/outstanding balances, assigned classes, published results, and recent announcements.
>
> Derive each metric from authoritative records and define its date/session/school filters explicitly. Do not expose financial details to roles without permission or draft results to guardians/students. Avoid N+1 queries and repeated per-student requests. Use database aggregates and targeted eager loading. Only add caching after documenting the key, tenant/session scope, TTL, and every mutation/event that invalidates it; never reuse data across school or user permissions.
>
> Add tests for metric correctness using seeded records, empty-state responses, date boundaries in Asia/Dhaka, authorization, and tenant isolation. Keep dashboards read-only; don't introduce business mutations through summary endpoints.
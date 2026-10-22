# Prompt 11 — Student attendance and leave

**Mode:** Plan, approve, implement.

> Implement student attendance for the approved academic enrollment model. Support date-based attendance by school, session, class, section, and optionally period only if the product decision includes it. Include configurable statuses such as present, absent, late, excused, and approved leave. Preserve who recorded or corrected attendance and when.
>
> Provide efficient class-roster retrieval and bulk attendance submission. Validate that every student belongs to the selected school/session/class/section and prevent duplicate attendance for the same defined attendance unit. Make bulk writes transactional. Use unique database constraints and safe upsert/duplicate handling without silently overwriting corrections. Record correction reason and actor for edits to submitted attendance.
>
> Include staff authorization for assigned classes, principal/admin override rules, date and holiday validation where configured, pagination for history/report lists, and tests for duplicate submissions, unauthorized students, invalid dates, partial payloads, concurrent requests, corrections, and cross-school access. If offline attendance is planned later, design stable IDs/idempotency semantics but do not build client-side offline functionality in this API task.
>
> Do not send real SMS/push notifications; emit a testable domain event/job contract if notification integration is needed.
# Prompt 12 — Exams, assessment schemes, marks, and results

**Mode:** Plan, approve, implement. Consider splitting into scheme/setup and marks/publication tasks if the plan is too large.

> Implement configurable examination and assessment workflows without hard-coding one Bangladesh curriculum. Support exam/term definitions, subject participation, assessment components, maximum marks, weights, grading-scale versions, pass rules, marks entry, absent/exempted/incomplete statuses, validation, review, approval, and publication.
>
> Validate that entered marks are within configured bounds and that assessment weights/rules are internally consistent. Clearly distinguish zero marks from absent, exempt, or missing marks. Store the grading/assessment scheme version used for a result so later policy changes do not silently change historical results. Restrict marks entry to authorized teachers/subjects/classes and result approval/publication to designated roles.
>
> Use transactions for approval/publication and maintain an audit trail for corrections. Do not publish incomplete results unless an explicit institution setting permits it. Build endpoints for exam setup, schedules, marks entry, review, publish, individual result, mark sheet, and class result summaries as appropriate to the approved plan.
>
> Tests must cover boundaries, missing marks, duplicate submissions, unauthorized editing, post-publication correction rules, recalculation consistency, and tenant/session isolation. Document formulas and assumptions; never invent official grading rules.
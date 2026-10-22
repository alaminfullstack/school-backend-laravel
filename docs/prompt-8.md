# Prompt 8 — Guardians, student accounts, and family access

**Mode:** Plan, approve, implement.

> Implement safe guardian/student identity linking and self-service API read access. A guardian may be related to more than one student, and a student may have multiple guardians with relationship and contact permissions. Use an explicit invitation/verification or admin-approved linking workflow; never link accounts merely because names match or phone numbers are equal.
>
> Guardians may read only their linked children's permitted profile, current enrollment, attendance summaries, timetable, published results, invoices, verified payment receipts, and school notices. Students may read only their own permitted information. Draft results, internal staff notes, restricted documents, and other families' data must never be exposed.
>
> Implement relationship authorization at the API/service/policy layer, with tests for direct-ID guessing, revoked guardians, multiple children, and users with both guardian and staff roles. Avoid making duplicated copies of authoritative student data. Document which data is intentionally available to guardians/students and at what lifecycle state.
>
> Do not implement payment processing, result calculations, or notification delivery in this task; use existing module contracts or placeholders only where required.
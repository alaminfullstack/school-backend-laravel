# Prompt 6 — Admissions and applicant workflow

**Mode:** Plan, approve, implement.

> Implement admissions as a complete, auditable workflow. Support configurable admission periods/forms, applications, applicants' Bangla/English names, guardian contacts, requested class/session, required-document metadata, review notes, admission status, waitlist/selection where configured, approval/rejection, and enrollment handoff.
>
> Use a controlled state transition model such as draft → submitted → under_review → approved/waitlisted/rejected → enrolled. Validate transitions on the server; prevent unauthorized direct status changes. A submitted application should not automatically create duplicate student or enrollment records. Approval/enrollment must be transactional and idempotent. Admission number/receipt allocation must be safe under concurrent requests.
>
> Support private document uploads only if storage is already configured, with file type/size validation, non-guessable access, authorization, and tests. Do not return raw file paths publicly. Include filters by admission cycle, status, class, and date; paginate all list endpoints.
>
> Add tests for each permitted/forbidden transition, duplicate submissions, concurrent/duplicate enrollment attempts, invalid documents, authorization, and tenant isolation. Document endpoint request/response examples and how an approved applicant becomes a student without duplicating identity data.
>
> Do not build the full student profile, fee collection, or exam module here except for the minimum enrollment handoff contract.
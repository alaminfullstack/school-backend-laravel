 We are building an API-first School Management System for schools in Bangladesh. Backend: Laravel REST API. Frontend is a separate React + Vite + TypeScript PWA, so this task is backend/API only. Support Bangla and English names/labels where appropriate, BDT, Asia/Dhaka timezone, academic sessions, classes, sections, shifts, configurable academic rules, and multiple institutions. The API should be consistent, secure, testable, and efficient. Inspect this repository and its installed versions before choosing implementation details. Do not upgrade the framework or add dependencies without explaining why and receiving approval.

 > - Re-read `agent.md`, the approved plan, the relevant existing code, migrations, routes, and tests before editing.
> - Implement only this module and the directly necessary integration points. Do not refactor unrelated code or begin another module.
> - Reuse established project conventions. Keep controllers thin; use Form Requests for input validation, API Resources/consistent transformers for responses, policies for authorization, and domain services/actions where they materially clarify business rules. Do not create needless abstraction layers.
> - All school-owned records must be scoped to the authenticated user's authorized school/tenant and, where applicable, campus and academic session. Never trust a `school_id`, role, price, fee amount, payment status, or permission supplied by the client without server-side verification.
> - Validate inputs on the server. Use database constraints and transactions for integrity-critical multi-step writes. Use pagination, explicit field selection, eager loading, and appropriate indexes. Avoid N+1 queries and unbounded collection responses.
> - Keep API response shapes and status codes consistent with the existing API contract. Document changed endpoints and example requests/responses.
> - Add feature tests for happy paths, validation, unauthorized access, cross-school access denial, and important edge cases. Add unit tests only for isolated complex rules. Do not weaken or delete existing tests just to make the suite pass.
> - Run focused tests first, then relevant broader tests, formatting/static checks already configured in the repo, and `git diff --check`. Never claim a test passed unless you actually ran it. Do not modify `.env` secrets or use production data.
> - Finish with: files changed; behavior implemented; endpoints added/changed; migrations; commands/tests executed and their actual result; assumptions; unresolved risks; manual verification steps. Stop after this module.

## Suggested execution order

1. Prompt 0 — Repository audit and API plan
2. Prompt 1 — `AGENTS.md`
3. Prompt 2 — API foundation
4. Prompt 3 — Authentication, roles, permissions
5. Prompt 4 — Institution/tenant/campus
6. Prompt 5 — Academic configuration
7. Prompt 6 — Admissions
8. Prompt 7 — Student records/enrollment history
9. Prompt 8 — Guardian/student access
10. Prompt 9 — Staff and teacher assignments
11. Prompt 10 — Timetable
12. Prompt 11 — Attendance
13. Prompt 12 — Exams/results
14. Prompt 13 — Fees and manual collections
15. Prompt 14 — Payment provider, only after finance rules are verified
16. Prompt 15 — Notifications
17. Prompt 16 — Dashboard
18. Prompt 17 — Reports/exports
19. Prompt 20 — Audit/security review (repeat after high-risk modules)
20. Prompt 21 — Performance review
21. Prompt 22 — OpenAPI/frontend contract
22. Prompt 18/19 — Optional modules as demanded by real customers
23. Prompt 23 — Release readiness
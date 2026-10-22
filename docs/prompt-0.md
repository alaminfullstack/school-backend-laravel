# Prompt 0 — Repository audit and API implementation plan

**Mode:** Plan / Ask. No application code changes.

> Act as a senior Laravel architect reviewing a new or existing API-first school ERP repository. Do not edit application files yet.
>
> 1. Inspect the repository, `composer.json`, Laravel/PHP versions, installed packages, route setup, authentication, database configuration, migrations, tests, formatter/static-analysis tools, and existing conventions. If the repository is empty or not yet a Laravel project, report that clearly and propose the smallest safe bootstrap path; do not assume.
> 2. Summarize the current architecture, what already exists, risks, and missing foundations.
> 3. Design a maintainable modular-monolith API for a Bangladesh-focused school system. Recommend module boundaries, directory conventions, API versioning, authentication approach, authorization strategy, tenant isolation, error format, pagination, file handling, queues, caching, and test strategy.
> 4. Propose a dependency-aware implementation order from foundation through identity/permissions, institution setup, academic configuration, admissions, students, attendance, exams/results, fees, notifications, reports, and optional modules.
> 5. Identify decisions that must be confirmed before implementation. Separate confirmed requirements from assumptions. Prefer safe defaults and do not ask questions whose answers can be discovered from the repository.
> 6. Produce a concise architecture decision record and implementation plan with milestones and acceptance criteria.
>
> Constraints: do not overengineer; start with a modular monolith, not microservices; do not add dependencies without justification; preserve the currently installed framework version; all external side effects must be mocked in tests. Do not write application code in this task.
>
> Deliver: repository findings, architecture decisions, proposed module dependency map, implementation sequence, risks, and a checklist for the first implementation task.
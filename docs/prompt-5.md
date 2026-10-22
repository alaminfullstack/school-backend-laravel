# Prompt 5 — Academic configuration (years, classes, sections, shifts, subjects)

**Mode:** Plan, approve, implement.

> Implement the academic configuration module. Support school-owned academic years/sessions, configurable class/grade levels, sections, shifts, subject catalogue, class-subject assignments, working days, holidays, and school calendar entries. Support multiple campuses if enabled by the approved schema.
>
> Make academic rules configurable rather than hard-coded for a single curriculum. Do not assume every school uses the same class names, grading system, class duration, weekday pattern, or subject set. Prevent duplicate active academic years or duplicate class/section identifiers within the appropriate school/session scope where the business rule requires it. Define how the current academic session is selected and how closed sessions become read-only or require elevated permission to edit.
>
> Create migrations, relationships, Form Requests, policies, API Resources, REST endpoints, factories/seeders where useful, and feature tests. Enforce school/campus scope and referential integrity. Add list filtering, sorting allowlists, and pagination. Include tests for overlapping/duplicate configuration, inactive/closed sessions, and cross-school access.
>
> Do not hard-code Bangladesh government curriculum rules. Record any curriculum/grade assumptions in the documentation. Do not implement admission, attendance, or exam workflows in this task.
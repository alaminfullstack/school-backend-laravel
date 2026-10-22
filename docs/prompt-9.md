# Prompt 9 — Staff directory and teacher assignments

**Mode:** Plan, approve, implement.

> Implement staff profiles and teaching assignments. Support employee identifier, Bangla/English name where needed, contact details, designation, department, employment status, joining/leaving details, qualifications as appropriate, and private document metadata. Assign teachers to school/campus, academic session, class/section, subject, and optionally period. Preserve historical assignments when a teacher changes role or school.
>
> Enforce permissions so HR/admin staff manage employment records while teachers see only authorized operational data. Limit sensitive fields in ordinary teacher-list responses. Prevent conflicting or duplicate assignment records within defined rules and validate that class, section, subject, school, and session relationships are compatible.
>
> Include pagination, useful filters, policies, validation, transactions where multiple related records are changed, migrations, resources, and tests for assignment conflicts, inactive staff, historical records, and tenant isolation.
>
> Do not implement payroll or complete timetable scheduling in this task.
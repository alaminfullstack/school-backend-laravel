# Prompt 10 — Timetable and scheduling

**Mode:** Plan, approve, implement.

> Implement school timetable configuration and read APIs. Support working days, periods/time ranges, class/section schedules, teacher assignments, subject assignments, room/classroom allocation if configured, and effective academic session dates.
>
> Prevent overlapping assignments for the same teacher, class/section, and room when those resources are enabled. Use clear server-side conflict validation and return understandable conflict details. Handle shift-based schedules and school-specific weekdays without assuming a universal timetable. Decide whether timetable changes are draft/published and ensure guardians/students see only published schedules.
>
> Optimize timetable retrieval for a class/week and teacher/week, but do not introduce caching until there is a reliable invalidation strategy. Include tests for overlaps, permitted parallel activities if the schema allows them, published/draft visibility, time boundaries, and tenant/session isolation.
>
> Do not build automated timetable optimization or attendance in this task.
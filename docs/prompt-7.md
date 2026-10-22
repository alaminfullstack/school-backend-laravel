# Prompt 7 — Student Information System (SIS) and enrollment history

**Mode:** Plan, approve, implement.

> Implement student records and academic enrollment as separate concepts. A student has a persistent identity; an enrollment associates that student with a school, academic session, class, section, roll number, and status. Support promotion to a new enrollment without overwriting historical class/session records.
>
> Include a practical Bangladesh school profile: student ID, Bangla/English name, photo metadata, date of birth, gender if required by institution, birth-registration identifier when required, addresses, guardian relationships, emergency contact, previous-school details, student status, and controlled documents. Collect only fields justified by product requirements; make optional/sensitive fields configurable where reasonable. Support siblings/guardians with relationships that do not expose unrelated children.
>
> Implement create/update/view/list/search endpoints, enrollment assignment/change history, transfer/withdrawal/archive status, and duplicate detection rules. Use database constraints for unique identifiers in the correct school scope. Do not use a student's roll number as a permanent global identifier. Define safe search behavior for Bangla and English names without promising transliteration matching unless implemented.
>
> Test student creation and updates, same student across academic sessions, duplicate IDs/roll numbers, guardian relationships, data visibility, file access if applicable, and cross-school isolation. Return only necessary fields and paginate/search server-side.
>
> Keep admission approval integration explicit; do not build attendance, fees, or marks here.
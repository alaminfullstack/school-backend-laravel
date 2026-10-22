# Prompt 20 — Audit trail and security review

**Mode:** Plan, approve, implement.

> Review and improve auditability for sensitive school ERP operations. Prioritize student record changes, guardian relationship changes, attendance corrections, marks/result changes and publication, fee/invoice/payment adjustments, refunds/reversals, permission changes, file access, and school settings changes.
>
> Record actor, school context, action, entity/type and identifier, timestamp, reason where required, and a minimal before/after representation that does not leak passwords, tokens, payment secrets, or unnecessary sensitive child data. Prevent ordinary users from editing/deleting audit events. Avoid logging request bodies wholesale. Define retention/access assumptions for owner review.
>
> Review authorization paths for IDOR/BOLA, cross-tenant leakage, mass assignment, unsafe file access, overbroad API resources, weak status transitions, and unbounded listing endpoints. Add regression tests for any issues fixed. Do not make sweeping refactors; prioritize verified findings and report residual risks.
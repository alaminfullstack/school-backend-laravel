# Prompt 4 — Institution/tenant, campus, and school settings

**Mode:** Plan, approve, implement.

> Implement the institution and tenant foundation for a multi-school SaaS School ERP.
>
> Model a school/institution, optional campuses/branches, school membership for users, and institution settings needed by later modules. Include configurable Bangla and English names where appropriate, contact details, address, logo/storage metadata, timezone defaulting to `Asia/Dhaka`, currency defaulting to BDT, locale, academic display preferences, and institution status. Do not store uploaded documents as public arbitrary paths.
>
> Choose and document a safe tenant model based on the current repository. For a shared database, every school-owned record must be tenant-scoped and related queries must derive authorized school context from the authenticated user/membership—not from a client-supplied school ID alone. Define how a user belonging to multiple schools selects an authorized active school. Platform administrators should use a separate, explicitly authorized path.
>
> Provide endpoints to read/update settings and manage campuses/memberships within the caller's permissions. Add database constraints and indexes, policies, resources, and tests proving users cannot read, alter, or infer another school's records, including by guessing IDs. Include seed data only for development/testing.
>
> Do not implement academic years, student admissions, or other business modules here. Explain migration/backfill implications if adding tenant IDs to existing tables.
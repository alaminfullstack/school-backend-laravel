# Prompt 2 — API foundation and project conventions

**Mode:** Plan, approve, implement.

> Implement the approved API foundation for the school ERP. First inspect the actual Laravel version and existing project setup; use the installed version's documented APIs and do not upgrade it.
>
> Scope:
> - Establish `/api/v1` routing using the repository's compatible Laravel routing conventions.
> - Establish consistent JSON response conventions for success, paginated lists, validation errors, not found, unauthorized, forbidden, and unexpected errors. Preserve Laravel-standard status codes and validation behavior where possible.
> - Configure API request/response conventions, timezone handling (`Asia/Dhaka` at the application/business layer), safe logging with sensitive fields redacted, health/readiness endpoints if appropriate, and pagination defaults/maxima.
> - Add a minimal API documentation approach that matches the current dependencies; propose OpenAPI generation rather than silently adding a package.
> - Establish test helpers/factories and a simple vertical-slice example only if necessary to prove the conventions.
> - Document environment variables and local setup without committing real secrets.
>
> Do not build student, finance, or academic features yet. Do not configure unsafe wildcard CORS or turn off CSRF/security controls for convenience. Do not add caching globally before resource-level cache rules exist.
>
> Acceptance criteria: API routes resolve as intended; response conventions are covered by tests; invalid JSON/API input returns a consistent machine-readable response; setup instructions are accurate; the full existing test suite still passes.
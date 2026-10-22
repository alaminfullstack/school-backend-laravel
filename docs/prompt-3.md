# Prompt 3 — Authentication, users, roles, and permissions

**Mode:** Plan, approve, implement.

> Implement authentication and authorization foundations for the school ERP API.
>
> First inspect how the React SPA will be deployed and the existing Laravel setup. Recommend and implement the appropriate supported Laravel authentication approach. For a first-party SPA on the same top-level domain, prefer Laravel Sanctum's cookie/session SPA flow with correct stateful-domain, CORS, and CSRF configuration. Use token authentication only for real non-browser clients that require it. Do not store long-lived secrets in browser local storage.
>
> Implement only the approved scope: login/logout, current-user endpoint, password reset flow if a mail service is configured (fake it in tests), account status, session/token revocation as applicable, role/permission assignment, and server-enforced policies/middleware. Use least-privilege defaults. Separate platform-level administrators from school-level roles. Roles should be configurable where reasonable; avoid scattering hard-coded role-name checks throughout controllers.
>
> Required access model: platform super admin; school owner/admin; principal; admission staff; accountant/cashier; teacher; exam controller; guardian; student; optional support staff. Enforce access through policies/permissions on every protected operation. A role shown in the UI is not a security boundary.
>
> Add tests for unauthenticated requests, invalid credentials, disabled users, role/permission denial, privilege escalation attempts, logout/session invalidation, and cross-school resource access denial. Avoid exposing password hashes, tokens, secrets, or unnecessary user fields in API resources.
>
> Do not build school, student, or finance modules in this task. Document authentication setup steps for the React SPA.
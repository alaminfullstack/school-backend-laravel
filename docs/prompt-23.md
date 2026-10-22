# Prompt 23 — Final end-to-end API verification and release readiness

**Mode:** Plan first; then execute safe checks.

> Audit the completed API against the approved requirements and actual implementation. Do not claim production readiness merely because the app boots.
>
> Verify: migrations from a clean test database; route list and API version consistency; authentication/session behavior; role/policy checks; tenant isolation; academic-session scoping; request validation; JSON resource output; duplicate/concurrent operations in attendance and finance; exam/result state transitions; private file access; queued jobs/provider fakes; cache invalidation; backups/restore documentation if present; rate limiting; log redaction; API documentation; and test coverage for critical workflows.
>
> Run the test suite and configured formatter/static checks. Use only local/test data and mocked providers. Do not deploy, access production systems, send SMS/email/push, or make payments. Report every command run and its actual result. Separate blockers, high/medium risks, and optional improvements. Fix only well-scoped issues approved for this task and avoid unrelated refactoring.
>
> Provide a release checklist and a manual end-to-end test script for: create school → configure academic session/class → admit/enroll student → assign teacher → record attendance → configure assessment and publish result → create invoice → record test payment → view permitted guardian data.
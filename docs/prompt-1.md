# Prompt 1 — Create repository-wide `AGENTS.md`

**Mode:** Plan first, then implement the documentation only.

> Create a concise root `AGENTS.md` that guides Codex throughout this Laravel API project. Before writing it, inspect the real repository and Prompt 0 decisions. Do not invent tools, directories, packages, coding standards, or commands that are not present or explicitly approved.
>
> Include: product context (Bangladesh school ERP, Laravel API, separate React/Vite PWA); project-specific commands; architectural boundaries; naming/style conventions; request validation and API response standards; authentication and policy requirements; school/tenant and academic-session scoping; database integrity; migration safety; performance guidance; test requirements; sensitive student data handling; external service fakes; and an instruction to implement one approved module at a time.
>
> Tell Codex to inspect existing code before changing it, avoid unrelated refactors, run relevant tests, report actual test results, and never claim unverified success. For large or ambiguous work, plan first and wait for approval before implementation. Never expose secrets or run production/destructive commands without explicit approval.
>
> Add only `AGENTS.md` in this task unless another documentation change is strictly necessary. Review it for contradictions, excessive length, and unsupported assumptions; run `git diff --check`.
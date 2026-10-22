# Prompt 21 — Performance review and cache plan

**Mode:** Ask/Plan first; implement only measured fixes.

> Audit the existing API for performance using the real code and representative test data. Do not begin by adding Redis cache to every endpoint. Identify slow/high-volume paths, N+1 queries, missing indexes, over-fetching, unbounded results, expensive aggregates, synchronous external calls, and oversized payloads.
>
> For each finding, provide evidence or a reproducible method, expected impact, risk, and smallest proposed change. Prioritize query improvements, pagination, selected columns, eager loading, composite indexes aligned with real filters, bulk operations, and queues for slow work. Add application-level caching only where staleness is acceptable and invalidation can be made correct.
>
> Any cache must have a documented cache key including school/tenant and academic session where relevant, correct permission scope, TTL rationale, and explicit invalidation triggers. Never cache user-specific/private responses in shared caches without safe partitioning; do not allow one school's dashboard to appear to another school. Avoid long-lived cache for payment status, fee balances, draft marks, or authorization decisions.
>
> Establish or run benchmarks where possible; report before/after measurements instead of promising arbitrary latency. Add tests for cache invalidation and tenant isolation if caching is introduced.
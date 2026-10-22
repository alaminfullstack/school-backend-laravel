# Prompt 15 — Notifications and announcements

**Mode:** Plan, approve, implement.

> Implement notification preferences, in-app notifications, school/class announcements, message templates in Bangla and English, and queue-backed delivery adapters for email/SMS/push where providers are configured. Support recipient targeting based on authorized school, class, section, guardian-student relationship, or staff membership.
>
> Queue slow provider calls. Use retries with sensible limits, failure tracking, deduplication/idempotency keys where appropriate, and delivery-status records that avoid storing unnecessary sensitive message content. Use fake providers in tests. Respect user preferences and configurable notification categories. Avoid leaking student results, fees, or personal details to an unverified number or unrelated guardian.
>
> If browser push is included, keep subscription management separate from in-app notifications and support revoked/expired subscriptions. Do not assume every provider supports Bangla Unicode or the same message length/pricing. Do not send real messages during tests or development unless explicitly approved.
>
> Add tests for recipient scoping, duplicate jobs, provider failures, retry behavior, preferences, and cross-school isolation. Keep announcement creation/reading separate from provider delivery status.
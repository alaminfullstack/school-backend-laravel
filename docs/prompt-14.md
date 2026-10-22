# Prompt 14 — Online payment provider abstraction (later, after fees are stable)

**Mode:** Plan, approve, implement with sandbox/fake responses only.

> Design and implement an extensible online payment integration layer for providers the business has confirmed (for example bKash, Nagad, Rocket, or an approved gateway). First inspect the provider's current official documentation and the merchant credentials/contract assumptions supplied by the project owner; do not guess endpoint URLs, callback signatures, or onboarding requirements.
>
> Model payment intent creation, pending/paid/failed/cancelled/expired states, provider reference, verified transaction reference, raw event metadata with secrets/redaction, idempotency, callback verification, and reconciliation. Verify provider-side transactions server-to-server and validate callback authenticity exactly as the provider documents. Browser redirects alone must never mark an invoice paid. Process repeated callbacks safely and prevent duplicate ledger entries.
>
> All tests must use HTTP fakes or provider fixtures; do not send real requests, make charges, or expose credentials. Add webhook/callback replay protection, signature-verification tests, timeout/failure handling, and manual reconciliation paths. Update environment documentation with placeholder variable names only.
>
> Keep finance ledger state authoritative and separate from provider transport code. Do not add a real provider until the provider and sandbox access are confirmed.

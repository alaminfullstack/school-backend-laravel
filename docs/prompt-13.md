# Prompt 13 — Fees, invoices, collections, discounts, and receipts

**Mode:** Plan, approve, implement. Finance is high-risk; split into fee setup/invoices and collection/reconciliation if needed.

> Implement a reliable fee-management module. Support configurable fee types and structures, billing schedules, student-specific invoices, installments where required, discounts/scholarships/waivers, due dates, late fees if enabled, partial payments, outstanding balances, printable receipt data, refunds/reversals under authorization, and collection reports. Use integer minor units for money where currency/provider rules allow, or a documented decimal strategy; never use binary floating-point for financial calculations.
>
> Preserve an auditable ledger. Do not silently delete or overwrite posted invoices/payments. Corrections should use controlled void/reversal/refund entries. Define invoice and receipt numbering with concurrency-safe allocation. Use database transactions and appropriate row locks for collection operations where needed. Calculate balances server-side; never trust client-provided totals or payment status.
>
> This task must not call live payment providers. Separate manual cash/bank entries from online payment intents. Prepare provider integration contracts only if approved. Include idempotency handling for payment registration and clear reconciliation status. Add tests for partial/full payment, overpayment rules, discounts, refunds/reversals, duplicate requests, concurrency, rounding, permissions, and tenant isolation.
>
> Document every financial state transition and provide sample API requests/responses. Do not build online payment callbacks in this task.
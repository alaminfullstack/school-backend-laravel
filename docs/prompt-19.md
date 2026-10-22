# Prompt 19 — Optional facilities module (library / transport / inventory)

**Mode:** Plan, approve, implement one submodule at a time.

> Implement only the named optional submodule: [LIBRARY / TRANSPORT / INVENTORY]. First inspect existing SIS, campus, student, staff, fee, and permission models, then propose a small plan.
>
> For LIBRARY: catalogue, book copies, issue/return, due date, renewals, overdue rules, loss/damage, and optional fines; ensure a physical copy cannot be issued twice concurrently.
>
> For TRANSPORT: vehicles, routes, stops, student allocations by session, drivers/staff, vehicle capacity, and optional transport billing; avoid collecting live location data unless specifically required and approved.
>
> For INVENTORY: item catalogue, locations, suppliers, stock movements, purchase records, adjustments with reasons, and stock reports; never let arbitrary edits silently rewrite stock history.
>
> Implement only the selected module. Follow existing conventions, add policies, migrations, resources, pagination, transaction-safe state changes, tests, and API examples. Enforce tenant/campus scope. Do not build the other two modules.
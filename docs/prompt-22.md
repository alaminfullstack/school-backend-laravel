# Prompt 22 — OpenAPI/API contract and frontend integration guide

**Mode:** Plan, approve, implement.

> Produce and maintain an accurate API contract for the implemented endpoints. Inspect actual routes, Form Requests, Resources, policies, and tests; never document endpoints that do not exist. Use an existing OpenAPI tool if the repository has one, or propose a specific dependency before installing it.
>
> Document authentication/CSRF expectations for the React + Vite first-party SPA, base URL, API version, pagination, search/filter/sort conventions, success/error response shape, validation errors, date/time/currency representation, file upload/download rules, role permissions, and representative requests/responses for each implemented module.
>
> Include a module endpoint matrix and frontend integration notes: query keys should include school/session context; after mutations, the frontend should invalidate only affected query families; payment/result/attendance state must be refreshed appropriately. Do not mix frontend implementation into this API task.
>
> Add a validation/check so docs do not drift where feasible. Finish by listing undocumented routes and assumptions rather than inventing answers.
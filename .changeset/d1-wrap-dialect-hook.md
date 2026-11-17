---
"@emdash-cms/cloudflare": minor
---

Adds an optional second argument to the D1 `createRequestScopedDb` export, `{ wrapDialect }`, so code that wraps the D1 adapter can layer its own Kysely dialect on top of the per-request D1 Sessions API session. Wrappers such as multi-tenant database layers can now keep read replicas, bookmark cookies and primary-pinned writes instead of falling back to the primary-only binding. Sites that use `d1()` directly are unaffected: without the argument the behavior is unchanged.

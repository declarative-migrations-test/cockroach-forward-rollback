# Test plan

- Verify repeated apply and rollback under CockroachDB transaction and DDL semantics across the supported happy-path states and canonical fixtures.
- Verify repeated apply and rollback under CockroachDB transaction and DDL semantics under retries, interruption, concurrency, offline operation, or partial failure.
- Verify repeated apply and rollback under CockroachDB transaction and DDL semantics preserves authorization, idempotency, integrity, observability, and actionable failure classification.

## Classification

- product regression
- blocked dependency
- harness regression

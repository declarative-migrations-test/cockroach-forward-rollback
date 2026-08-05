# CockroachDB rollback end-to-end certification

This repository continuously certifies `declarative-migrations/declarative-postgres-migrate.rs` against a live CockroachDB instance.

The workflow pins production commit `21eb846e356b2a5aff068b21e77903e6cca50452`, builds the real `dpm` CLI, and exercises repeated forward migrations, gated destructive rollback, approved rollback, idempotency, final convergence, and row preservation on CockroachDB 25.2.4.

## Local run

```bash
docker run --rm -d --name dm-cockroach -p 26257:26257 cockroachdb/cockroach:v25.2.4 start-single-node --insecure
scripts/build-dpm.sh
DPM_BIN="$PWD/vendor/dpm/target/release/dpm" scripts/test-cockroachdb-rollback.sh
```

The test creates and removes its own throwaway database.

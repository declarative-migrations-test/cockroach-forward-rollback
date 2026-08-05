# AGENTS.md

Keep the production dependency pinned to `declarative-migrations/declarative-postgres-migrate.rs@21eb846e356b2a5aff068b21e77903e6cca50452` unless a reviewed dependency-update pull request advances it. Preserve CockroachDB-specific assertions, use only throwaway databases, distinguish gated destructive drift from convergence, and never weaken a rollback or data-preservation assertion merely to make CI green.

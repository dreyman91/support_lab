# Architectural decision log

Document decisions as they are made, not retrospectively.

## ADR-001 — Start with one service and one database
- **Status:** Proposed
- **Context:** Need to practise diagnosis, not maximize system complexity.
- **Decision:** Start with a FastAPI ticket API and PostgreSQL under Docker Compose.
- **Alternatives:** Microservices, Kubernetes, managed cloud databases.
- **Reasoning:** Smaller local setup provides controlled failure reproduction and observability.
- **Revisit when:** Four core incidents have reproducible runbooks and recovery tests.

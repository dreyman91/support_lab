# Roadmap

The schedule is an estimate; advance based on verified completion, not dates.

## Phase 1 — Working service (weeks 1–2)
- [ ] Agree API contract: authentication, tickets, health endpoints.
- [ ] Create FastAPI app structure and environment config.
- [ ] Connect PostgreSQL with migrations.
- [ ] Add secure password hashing/JWT and object-level authorization.
- [ ] Add unit + integration tests.
**Exit criteria:** normal operations pass locally and tests prove key behavior.

## Phase 2 — Reproducibility (week 3)
- [ ] Docker Compose API + PostgreSQL services with health checks.
- [ ] JSON logs containing request IDs and useful error classification.
- [ ] Separate liveness and readiness checks.
- [ ] Document baseline startup and smoke test commands.
**Exit criteria:** new clone can start and verify the service using documentation.

## Phase 3 — Evidence-driven incidents (week 4)
- [ ] INC-001 wrong database hostname (DNS).
- [ ] INC-002 invalid/expired JWT (authentication).
- [ ] INC-003 database container stopped (outage).
- [ ] INC-004 invalid required configuration (startup/readiness).
- [ ] Complete evidence, hypothesis, recovery, and verification runbooks.
**Exit criteria:** all four failures independently reproducible and recoverable.

## Phase 4 — Diagnostics + monitoring (weeks 5–6)
- [ ] Read-only `supportdiag` CLI gathers health, container state, logs, and metadata.
- [ ] Rule-based findings separate confirmed facts from possible causes.
- [ ] Prometheus request metrics and Grafana dashboard.
- [ ] Add alert tests for sustained errors/readiness problems.
**Exit criteria:** report and dashboard help investigate a reproduced incident.

## Phase 5 — CI + publish (weeks 7–8)
- [ ] GitHub Actions checks lint, unit, integration tests, container build.
- [ ] Add automated recovery regression checks.
- [ ] Compare manual versus automated diagnosis on repeated trials.
- [ ] Record a short demo; review docs and remove secrets/sensitive data.
**Exit criteria:** public repo has a complete reproducible demonstration.

## Optional extension after MVP
Toxiproxy fault latency, stale DB connection recovery, version mismatch, OpenTelemetry, SLO error-budget exercise.

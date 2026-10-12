# Roadmap

The schedule is an estimate; advance based on verified completion, not dates.

## Phase 1 — Working service (weeks 1–2)
- [ ] P1-T01 — Agree API contract: authentication, tickets, health endpoints.
- [ ] P1-T02 — Create FastAPI app structure and environment config.
- [ ] P1-T03 — Connect PostgreSQL with migrations.
- [ ] P1-T04 — Add secure password hashing/JWT and object-level authorization.
- [ ] P1-T05 — Add unit + integration tests.
**Exit criteria:** normal operations pass locally and tests prove key behavior.

## Phase 2 — Reproducibility (week 3)
- [ ] P2-T01 — Docker Compose API + PostgreSQL services with health checks.
- [ ] P2-T02 — JSON logs containing request IDs and useful error classification.
- [ ] P2-T03 — Separate liveness and readiness checks.
- [ ] P2-T04 — Document baseline startup and smoke test commands.
**Exit criteria:** new clone can start and verify the service using documentation.

## Phase 3 — Evidence-driven incidents (week 4)
- [ ] P3-T01 — INC-001 wrong database hostname (DNS).
- [ ] P3-T02 — INC-002 invalid/expired JWT (authentication).
- [ ] P3-T03 — INC-003 database container stopped (outage).
- [ ] P3-T04 — INC-004 invalid required configuration (startup/readiness).
- [ ] P3-T05 — Complete evidence, hypothesis, recovery, and verification runbooks.
**Exit criteria:** all four failures independently reproducible and recoverable.

## Phase 4 — Diagnostics + monitoring (weeks 5–6)
- [ ] P4-T01 — Read-only `supportdiag` CLI gathers health, container state, logs, and metadata.
- [ ] P4-T02 — Rule-based findings separate confirmed facts from possible causes.
- [ ] P4-T03 — Prometheus request metrics and Grafana dashboard.
- [ ] P4-T04 — Add alert tests for sustained errors/readiness problems.
**Exit criteria:** report and dashboard help investigate a reproduced incident.

## Phase 5 — CI + publish (weeks 7–8)
- [ ] P5-T01 — GitHub Actions checks lint, unit, integration tests, container build.
- [ ] P5-T02 — Add automated recovery regression checks.
- [ ] P5-T03 — Compare manual versus automated diagnosis on repeated trials.
- [ ] P5-T04 — Record a short demo; review docs and remove secrets/sensitive data.
**Exit criteria:** public repo has a complete reproducible demonstration.

## Optional extension after MVP
Toxiproxy fault latency, stale DB connection recovery, version mismatch, OpenTelemetry, SLO error-budget exercise.

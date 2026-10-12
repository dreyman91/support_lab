# SupportLab — Technical Support & Incident Response Lab

A learning-first portfolio project demonstrating evidence-based API troubleshooting, reproducible incidents, diagnostic automation, monitoring, testing, and recovery verification.

## Purpose
Build a small authenticated ticket API, then investigate and resolve deliberately introduced failures as if supporting a production service. This is an independent learning project, **not** a representation of any employer's systems.

## Planned stack
Python 3, FastAPI, PostgreSQL, SQLAlchemy/Alembic, Docker Compose, pytest, GitHub Actions, structured JSON logs, Prometheus/Grafana, and a Python diagnostic CLI (`supportdiag`). Add Toxiproxy only when introducing network faults.

## Definition of done (first portfolio release)
- Authenticated ticket API runs with PostgreSQL using Docker Compose.
- At least four faults are reproducible: DNS, authentication, database outage, configuration.
- Every fault has a runbook with symptoms, original evidence, hypotheses, confirmed cause, repair, and recovery test.
- `supportdiag` collects evidence and generates a report without inventing causes.
- Tests and a CI pipeline pass.
- No real customer data, credentials, employer configurations, or confidential logs appear in the repository.

## How to work
1. Read `docs/PROJECT_BRIEF.md` and `docs/ROADMAP.md`.
2. Use `chatgpt/PROJECT_INSTRUCTIONS.md` as custom instructions in a dedicated ChatGPT Project.
3. Keep `docs/PROGRESS.md` updated at the end of each working session.
4. Record architectural trade-offs in `docs/DECISIONS.md`.
5. Use `docs/INCIDENT_RUNBOOK_TEMPLATE.md` for every fault.
6. Implement one testable vertical slice at a time. This starter contains **no completed app** by design.

## Next task
Phase 1, Task 1: Decide the smallest API contract and define a local development environment (Python version, Docker and Compose versions). Do not introduce observability infrastructure yet.

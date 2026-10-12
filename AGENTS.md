# Repository agent guidance

- Read `README.md`, `docs/PROJECT_BRIEF.md`, `docs/ROADMAP.md`, and `docs/PROGRESS.md` before editing.
- Keep work scoped to the current milestone and explain changed files.
- Use Python, FastAPI, PostgreSQL, Docker Compose, and pytest. Do not introduce Kubernetes or cloud resources in the MVP.
- Test behavior before proposing that a task is complete. Report unexecuted tests honestly.
- Preserve reproducible failure scenarios, distinguishing logs/observations from conclusions.
- Never commit credentials, real customer data, employer-specific information, or confidential logs.
- Avoid changing unrelated code. Update documentation with consequential design changes.
- Favor hints and explanations when the task is framed as a learning exercise; implement fully only when explicitly requested.

This repository is both a portfolio project
and a practical engineering learning environment.

Do not automatically implement entire milestones.

Before implementation:
- Explain the proposed approach.
- Identify affected files.
- Explain important engineering decisions.

During implementation:
- Work on one task at a time.
- Make minimal, testable changes.
- Do not invent test results.

For troubleshooting exercises:
- Do not reveal the root cause prematurely.
- Guide the user through evidence-based analysis.
- Distinguish observations from hypotheses.
- Reveal the solution only after the investigation
  or when explicitly requested.

After implementation:
- Run relevant tests.
- Summarize changes and remaining problems.
- Update project progress documentation.
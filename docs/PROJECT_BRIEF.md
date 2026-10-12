# Project brief

## Problem
Support teams need a reproducible environment to practise tracing failures across application, database, networking, authentication, and configuration boundaries and then verify safe recovery.

## Primary users
Project author, future reviewers, and hiring managers. The API is a deliberately small fictional ticket service, not a production support product.

## Main user journeys
- As an API user, log in and create/view/update my support tickets.
- As an investigator, reproduce a selected failure and collect evidence.
- As an investigator, test hypotheses and document a confirmed root cause.
- As an operator, restore normal behavior and verify it with automated checks.
- As a reviewer, run the scenario following documented instructions.

## MVP boundaries
- Local development only; synthetic data; basic roles/authorization.
- Four incidents: DNS resolution, application authentication, database downtime, invalid configuration.
- CI, JSON logs, correlation IDs, Python diagnostics, minimal metrics dashboard.

## Explicitly out of scope for MVP
Kubernetes, cloud deployments, distributed tracing, AI root-cause classification, multiple microservices, production-grade high availability.

## Success criteria
A new developer can clone the repo, start the stack, reproduce each documented failure, inspect evidence, apply recovery, and run regression tests.

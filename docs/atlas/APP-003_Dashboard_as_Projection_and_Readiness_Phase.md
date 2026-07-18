# APP-003 — Dashboard as Projection and Readiness Phase

A dashboard is not the business or system. A green tile is also not automatically a readiness phase.

## Combined question

> Can materially different source configurations project the same visible dashboard state while belonging to different operational phases?

## Review

- identify metric definitions, aggregation windows, freshness, missingness, and source systems;
- construct the reconstruction fibre for the visible state;
- define the readiness or health phase criterion;
- test whether all admitted source candidates support the same phase;
- inspect whether the metric or probe changes the system it reports;
- require drill-down or another view when the phase spread is greater than one.

## Blocked overreads

- green is not healthy;
- threshold passage is not causal explanation;
- one metric is not a viability envelope;
- a published status is not performed work or authorisation.

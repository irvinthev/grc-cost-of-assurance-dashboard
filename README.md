# GRC Cost of Assurance Dashboard

This is a lightweight proof-of-concept dashboard for a GRC Engineering workflow.

## Live Demos

- Executive dashboard: https://irvinthev.github.io/grc-cost-of-assurance-dashboard/
- Scenario runner: https://irvinthev.github.io/grc-cost-of-assurance-dashboard/scenario-demo.html

It demonstrates how vendor and AI tool review activity can be translated into:

- process metrics
- evidence reliability
- remediation status
- estimated cost of assurance
- executive reporting

The dashboard uses sample data and visible assumptions. It is not a production GRC platform and should not be presented as audited savings. The purpose is to show how a messy workflow can be instrumented, measured, validated, and explained in business terms.

## Demo Story

The workflow follows a simple path:

1. Vendor / AI tool intake
2. Risk classification
3. Control mapping
4. Evidence validation
5. Risk register entry
6. ServiceNow-style remediation routing
7. Executive dashboard reporting

## Scenario Runner

The scenario runner lets you test three canned examples:

- Positive run
- Data validation error
- High-risk submission

It also includes a small intake form where you can submit a custom vendor/tool review using:

- vendor/tool name
- data type
- AI usage
- integration or permission level
- evidence status

The demo then calculates a simple risk score and updates:

- review result
- risk tier
- evidence health
- manual cost estimate
- cycle time
- event log
- control framework mapping
- risk register / remediation payload
- dashboard impact

This is intentionally simplified. The goal is to demonstrate the operating model, not to claim the scoring logic is production-ready.

The cost model is intentionally transparent:

```text
Manual labor cost = manual touches x average minutes x loaded hourly rate
Evidence rework cost = failed evidence x rework minutes x loaded hourly rate
Net avoided effort = manual cost avoided - runtime cost - maintenance effort
```

## Interview Positioning

This is not meant to prove a real dollar savings claim.

It is meant to show the operating model:

```text
workflow events -> process metrics -> cost model -> executive dashboard
```

That makes the cost story more defensible because the dashboard starts with observable workflow activity before translating it into estimated business impact.

## Suggested Demo Talk Track

I would present this as a proof-of-concept for how GRC Engineering can reduce the cost of assurance.

The key idea is not that the prototype proves real savings. The key idea is that the workflow makes GRC activity measurable:

```text
intake -> classification -> evidence validation -> control mapping -> exception/risk entry -> remediation routing -> dashboard impact
```

That creates a defensible way to explain cost, velocity, evidence reliability, and residual risk.

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

## How to Demo This

1. Open the executive dashboard and explain the business question: how much manual assurance effort is being created by vendor and AI tool reviews?
2. Open the scenario runner.
3. Run the positive submission to show the happy path.
4. Run the data validation error to show evidence quality controls.
5. Run the high-risk submission to show escalation, risk register entry, and remediation routing.
6. Use the dashboard impact section to explain cost, velocity, evidence reliability, and residual risk.

The point of the demo is not that this prototype is production-ready. The point is that the workflow makes manual GRC activity measurable and easier to manage.

## Example Validation Matrix

| Scenario | Expected Result | Example Controls Mapped | Risk Outcome | Cost Impact | Status |
| --- | --- | --- | --- | --- | --- |
| Positive vendor review | Review passes with complete evidence | Vendor risk, access governance, evidence reliability | Low residual risk | Manual review effort reduced | Pass |
| Data validation error | Submission is blocked or routed for correction | Evidence reliability, data quality, audit trail | Medium risk until corrected | Rework cost is visible | Pass |
| High-risk AI vendor | Review escalates to risk register and remediation | AI governance, data handling, vendor risk, incident response | High residual risk until mitigated | Cost of review and remediation is visible | Pass |

## Sample Evidence

The `sample-evidence` folder includes example evidence notes for each scenario:

- `positive-vendor.md`
- `missing-evidence.md`
- `high-risk-ai-vendor.md`

These are not real vendor records. They are test fixtures that explain the assumptions behind each scenario and make the demo easier to walk through.

## Cost Model

The cost model is intentionally transparent:

```text
Manual labor cost = manual touches x average minutes x loaded hourly rate
Evidence rework cost = failed evidence x rework minutes x loaded hourly rate
Net avoided effort = manual cost avoided - runtime cost - maintenance effort
```

## Portfolio Positioning

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

# High-Risk AI Vendor Evidence

## Scenario

An AI-enabled vendor review is submitted for a tool that may process sensitive data, use broad integrations, or introduce unclear data handling and model governance risks.

## Intake Summary

- Vendor/tool type: AI-enabled SaaS or automation platform
- Data handled: Customer, employee, confidential, or regulated data
- AI usage: Generates, summarizes, classifies, or acts on business data
- Integration level: Broad API, admin, plugin, or workflow automation permissions
- Evidence status: Partial or insufficient for the requested use case

## Expected Result

The workflow should classify the submission as high risk, create a risk register entry, and route remediation before approval.

## Evidence Assumptions

- Data retention and training usage are unclear.
- Integration permissions exceed the stated business need.
- Evidence does not clearly support the vendor's AI governance claims.
- No documented review exists for human oversight, output validation, or incident escalation.
- The proposed use case may expose sensitive data or trigger downstream business actions.

## Example Control Mapping

| Control Area | Example Expectation | Result |
| --- | --- | --- |
| AI governance | AI use case, data handling, and oversight are documented | Fail |
| Vendor risk | High-risk vendor review is completed before approval | Needs escalation |
| Access governance | Permissions are least-privilege and justified | Fail |
| Data governance | Sensitive data use is approved and documented | Needs review |
| Incident response | Escalation path exists for AI/vendor issues | Needs review |

## Dashboard Impact

- Higher review cost
- Longer cycle time
- High residual risk until mitigated
- Remediation routed to a ServiceNow-style queue
- Risk register entry created for tracking ownership and status

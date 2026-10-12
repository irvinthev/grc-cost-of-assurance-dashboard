# Data Validation Error Evidence

## Scenario

A vendor review is submitted with incomplete or conflicting evidence. The intake may look reasonable, but the supporting documentation does not fully back up the vendor's answers.

## Intake Summary

- Vendor/tool type: SaaS vendor
- Data handled: Internal or customer-related data
- AI usage: Not applicable or unclear
- Integration level: API integration requested
- Evidence status: Missing or conflicting

## Expected Result

The workflow should flag the issue and route the review for correction before the vendor is treated as approved.

## Evidence Assumptions

- Questionnaire answer says encryption is enabled, but no supporting documentation is attached.
- Access permissions are described at a high level but not tied to actual integration scope.
- SOC 2 or equivalent report is missing, expired, or not reviewed.
- Required fields are incomplete.

## Example Control Mapping

| Control Area | Example Expectation | Result |
| --- | --- | --- |
| Evidence reliability | Claims are supported by documentation | Fail |
| Data quality | Required fields are complete | Fail |
| Vendor risk | Risk tier can be assigned from reliable inputs | Needs review |
| Audit trail | Exception is logged for follow-up | Pass |

## Dashboard Impact

- Increased evidence rework
- Longer cycle time
- Medium residual risk until corrected
- More visible cost of manual follow-up

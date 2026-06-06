# Clarifications Required

Based on the latest requirement document (`Requirements/Proposal Info.xlsx`), test cases were generated with explicit assumptions where details are missing.

## Critical clarifications required

1. Exact workflow statuses and transitions for Proposal Info screen (Draft, Submitted, Rework, Approved, Rejected, Confirmed) are not explicitly defined.
2. Final role matrix (Maker/Checker/Viewer/Approver permissions) for Edit, Submit, Approve, Reject, Confirm actions is not provided.
3. Exact validation messages and error codes are not provided for each field-level validation.
4. Date format standard and timezone handling rules are not explicitly specified.
5. Numeric field constraints (min/max ranges, decimal handling, max length) are not defined for dosage/amount/month fields.
6. Maximum allowed length and special character policy are not defined for manual VARCHAR fields.
7. Behavior for API failure/timeout/retry (Deposit API, Liability API, Lead details API) is not documented.
8. Audit logging and user notification expectations for integration failures are not documented.
9. Confirm action trigger stage and post-confirm business behavior are not specified.
10. Delete/Upload applicability in Proposal Info - Other Details section is not explicitly documented.

## Assumptions used for test generation

- Maker-Checker flow applies for submit/approve/reject lifecycle.
- Non-editable fields remain read-only for all roles and all stages.
- Future date is not allowed for `Relationship Since`; same future-date restriction was assumed for SHG resolution date unless otherwise configured.
- Standard mandatory validation behavior is expected on Save/Submit.
- Controlled error handling is expected for integration failures without UI crash.

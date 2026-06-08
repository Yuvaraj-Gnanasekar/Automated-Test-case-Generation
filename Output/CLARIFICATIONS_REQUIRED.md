# Clarifications Required

## Requirement Gaps Identified
1. Workflow stages are not explicitly defined (for example, exact statuses, transitions, and approval hierarchy).
2. Role matrix is not provided (Maker/Checker/Viewer permissions are assumed for test coverage).
3. Validation message text is not provided for most fields, only validation intent is available.
4. Maximum length constraints are not specified for most VARCHAR/Text Area fields.
5. Duplicate-check rules are not specified for SHG records, employee selection, or borrower row entries.
6. Print output format/content specification is not provided for SHG Visit report.
7. API error code mapping and retry limits are not defined for HRMS/Party/Facility/Proposal integrations.
8. Save vs Submit button behavior in workflow is not fully described in the requirement sheet.
9. Borrower details table row-level rules (duplicate person prevention, max rows, mandatory combination logic) are not defined.

## Assumptions Applied for Test Case Generation
1. SHG Visit module follows role-based access control with at least Maker, Checker, and Viewer personas.
2. Mandatory field validation blocks both Save and Submit where business-critical data is missing.
3. Auto-populated and non-editable fields are sourced from upstream systems and cannot be overridden manually.
4. Standard validation behavior applies (type, format, boundary, and null checks) when explicit rules are absent.
5. Integration failures are shown as user-facing alerts and allow controlled retry without duplicate record creation.
6. Print button generates SHG Visit report with latest saved data snapshot.

## Generation Summary
- Total test cases generated: 321
- Coverage includes: screen-wise, field-wise, button-wise, validation-wise, workflow-wise, role-wise, integration-wise, and end-to-end scenarios.
- Test cases are intentionally split so each validation/assertion is covered in a separate case.

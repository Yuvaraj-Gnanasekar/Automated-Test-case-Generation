# Clarifications Required

1. Confirm the exact role matrix (Maker/Checker/Approver/Viewer) for SHG Party Details, including which roles can Edit, Submit, Delete, Approve, and Reject.
2. Confirm exact validation rules for each text field: minimum length, maximum length, allowed special characters, and whether leading zeros are permitted for numeric fields.
3. Confirm numeric constraints for all amount/count fields: decimal allowance, negative value handling, and maximum permissible value.
4. Confirm whether `Unique code of SHG` requires uniqueness validation across branch/region/CBS and whether format rules exist.
5. Provide LOV master data for Social Category, Caste, Community, Profession/Activity, and confirm whether these lists are branch-specific.
6. Confirm whether Gender LOV for SHG non-individual should be restricted to Male/Female only or include additional values.
7. Confirm CKYC No format and validation pattern (length, alphanumeric constraints, checksum if any).
8. Confirm integration behavior with CBS for CKYC fetch: trigger point, timeout threshold, retry count, and fallback behavior.
9. Confirm if stage `Under Review` exists in workflow or if status path is only Draft > Submitted > Approved/Rejected.
10. Confirm if delete operation is soft delete or hard delete and whether audit/log retention is mandatory.
11. Confirm expected validation/error message text for mandatory, invalid format, duplicate designation, and integration failure scenarios.
12. Confirm whether co-applicant cap exists when Designation values are exhausted (after President/Secretary/Treasurer are assigned).
13. Confirm whether totals/cross-field checks are required among income, expenditure, and repayment fields (e.g., repayment <= income).

## Assumptions Used for Test Generation

- Standard Party Details actions (Add, Save, Submit, Edit, Cancel, Delete, Approve, Reject) are available in the workflow.
- Numeric fields are treated as integer-only unless explicitly stated otherwise.
- Text fields use configuration-driven max length and disallow unsupported special characters.
- Workflow includes maker-checker processing with status transitions and alert messages.
- CKYC may be manually entered when CBS does not return a value.

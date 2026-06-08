# Clarifications Required

1. Confirm exact character length limits (minimum/maximum) for manual text fields:
   - Last CC Dosage / Linkage
   - Last CC Dosage Amount
   - Period Lapsed from release of last DP (Months)
   - Last TL Dosage / Linkage
   - Last TL Dosage Amount
   - Facilitating Agency Name

2. Confirm allowed character set for manual text inputs (alphanumeric only vs specific special characters) for:
   - Facilitating Agency Name

3. Confirm whether negative numeric values and decimal values are allowed for dosage/amount/month fields.

4. Confirm complete role matrix for Proposal Info actions (Maker/Checker/Approver/Viewer) including permissions for Save, Submit, Edit, Approve, Reject, Confirm.

5. Confirm whether Cancel, Confirm, unsaved-change warning, and success toast behaviors are implemented on this screen.

6. Confirm exact validation rule for Date of SHG Resolution (future date allowed or not; should it be <= application date).

7. Confirm integration failure behavior expectations:
   - Retry attempt count
   - timeout threshold
   - user-facing message text

8. Confirm whether audit log/reporting requirements exist for data changes in Other Details and API fetch failures.

9. Confirm precise business rules for stage reversal/return flow and status names used in workflow timeline.

10. Confirm narrative formatting template for "Present Proposal in Brief" when multiple facilities exist and sanction amount is partially available.

## Assumptions Used While Generating Test Cases

- SHG-specific fields are hidden for non-SHG schemes.
- Auto-populated fields from APIs are non-editable unless stated otherwise.
- Auto-calculated dosage fields are non-editable and recomputed from source dosage values.
- Role-based access includes Maker, Checker, Approver, and View-only users.
- Standard validation UX includes field-level errors and user-friendly alert/toast messages.
- Status lifecycle includes Draft, Submitted, Returned, Approved, and Rejected states.

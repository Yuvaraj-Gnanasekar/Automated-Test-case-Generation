# Clarifications Required

Based on `Requirements/Proposal Info.xlsx`, the following clarifications are needed while test cases were generated with reasonable assumptions:

1. Confirm exact user role names and permission matrix for Proposal Info actions (Maker/Checker/Viewer used as assumption).
2. Confirm exact button set available on Proposal Info > Other Details (Save/Submit/Cancel/Edit/Confirm assumed for coverage).
3. Provide exact validation messages for each mandatory and datatype validation.
4. Confirm allowed numeric ranges and max lengths for numeric text fields (dosage, amount, period).
5. Confirm allowed max length and character rules for text fields (Facilitating Agency Name, PNB Sakhi, etc.).
6. Confirm whether decimal values are allowed in numeric fields or only integers.
7. Confirm behavior when both Existing CC and Existing TL accounts are absent for SHG proposal.
8. Confirm retry mechanism UI behavior for Deposit API and Liability API failures (manual retry button vs automatic retry).
9. Confirm status lifecycle names and transition rules beyond Draft/Submitted/Returned (if any additional states exist).
10. Confirm whether audit trail/history visibility is required on this screen for field-level changes.
11. Confirm exact narrative format token values for "Present Proposal in Brief" in multi-facility scenarios.
12. Confirm whether `MCP` and `Insurance Coverage Obtained` default should auto-lock only at `Current Dosage/Linkage >= 3` for both CC and TL paths in all cases.

## Assumptions Used

- SHG scheme selection controls visibility of the entire Other Details section and all SHG-specific fields.
- Standard workflow actions and role-based controls exist as typically implemented in proposal systems.
- API failures are surfaced with user-facing alerts and logged for diagnostics.
- Persisted data is expected to remain consistent across save, submit, return, and reopen actions.

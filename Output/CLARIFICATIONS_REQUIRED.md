# Clarifications Required - SHG Grading Calculation

Based on `Requirements/Grading SHG.xlsx`, detailed test cases were generated with explicit assumptions where information is missing. Please confirm the following critical points:

1. **Role matrix**: Exact actors and permissions are not defined (Maker/Checker/Viewer assumptions used).
2. **UI actions**: Button names and availability (Calculate, Save, Submit, Approve, Reject, Reset, Export, Fetch Latest Data) are not explicitly documented.
3. **Rounding rule**: Decimal precision and rounding/truncation rule for each indicator score and total score are not specified.
4. **Score capping behavior**: Clarify whether every indicator is hard-capped at allotted marks for ratios above thresholds.
5. **Final grade outcome**: Grade bands/status mapping from total score (e.g., A/B/C or Pass/Fail) is missing.
6. **Validation messages**: Exact text for mandatory, range, format, and integration error alerts is not provided.
7. **Workflow lifecycle**: Draft/submitted/approved/rejected status flow and reversal/rework rules are not explicitly defined.
8. **Integration contracts**: API/event specifications, retry limits, timeout values, and fallback behavior for source modules are missing.
9. **Record-keeping scoring detail**: For some books, only partial mapping is visible; confirm exact full/half/zero mark logic per book across all dose types.
10. **Boundary interpretation**: Confirm inclusivity for threshold boundaries (e.g., exactly 1.5, exactly 0.5, exactly 2 occasions, exactly 3 occasions).
11. **Term loan overdue logic**: Requirement text has inconsistent wording around occasion counts; confirm the exact band definitions.

## Assumptions Used for Test Case Expansion

- SHG grading module supports maker-checker governance and audit trail.
- Source data is pulled from mapped modules and can be manually retried on failure.
- Score calculation is trigger-based (calculate action) and report export is available post-approval.
- Numeric inputs disallow negative and non-numeric values.

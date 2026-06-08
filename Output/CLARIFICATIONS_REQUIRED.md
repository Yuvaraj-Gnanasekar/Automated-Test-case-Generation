# Clarifications Required

Based on `Requirements/Agri details.xlsx`, the following critical clarifications are required while test cases were generated using standard assumptions:

1. **Role-permission matrix is not defined**
   - Roles allowed to Create/Edit/Submit/Approve are not explicitly specified.
   - Assumed maker-checker-viewer style control for permission and workflow test coverage.

2. **Button/action inventory is not explicitly documented**
   - Save/Submit/Edit/Cancel/Back actions are not directly listed in the requirement sheet.
   - Test cases were generated with standard transactional action assumptions.

3. **Exact validation boundaries are missing for numeric fields**
   - Minimum and maximum allowed values are not defined for manual numeric inputs.
   - Boundary test cases are included with configurable-rule assumptions.

4. **Date validation rules are incomplete**
   - Allowed date range for `Balance Sheet as on` is not specified (past-only, current date, future date behavior).

5. **Workflow status model is not defined**
   - Explicit status names and transition rules are missing.
   - Assumed Draft, Submitted, Rework/Rejected, Approved for workflow coverage.

6. **Integration error-handling behavior is incomplete**
   - CBS timeout/retry/error-message behavior for `Deposit with Bank` is not explicitly defined.
   - Retry/error handling test cases included as assumption-based integration coverage.

7. **Validation message text is not provided**
   - Exact user-facing error/success messages are not listed for mandatory or invalid input scenarios.

8. **Checklist enforcement moment needs confirmation**
   - Requirement states save is allowed only when checklist is complete, but does not specify whether validation is triggered on Save only or also on Submit.

9. **Dropdown LOV governance details are missing**
   - LOV source and whether options are configurable at runtime is not mentioned.

10. **Audit and logging requirements are not detailed**
    - No explicit specification on who changed what/when for critical tab edits and submission actions.

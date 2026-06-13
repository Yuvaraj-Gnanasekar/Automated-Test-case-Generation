# Clarifications Required

1. The requirement document is predominantly scheme-specific to KCC/KSY. Please confirm if generic/common validations from shared screens should continue to be executed for non-KCC/non-KSY schemes when scheme fields are excluded.
2. Several sections refer to screenshots/images for UI behavior and messages. Please provide text-level details for any mandatory validations/messages that appear only in images.
3. Role-permission matrix is referenced functionally (maker/checker/approver/operations) but not provided as a formal matrix. Please share exact role-to-screen/action mapping for negative permission validation completeness.
4. Integration error code catalog is not specified (Dedupe/CIF/Deposit/Liability/Loan Account services). Please provide expected error codes/messages and retry limits per service.
5. Document upload constraints (file type, max file size, scan quality rules, malware checks) are not explicitly defined. Please provide exact validation rules for upload-related negative tests.
6. Boundary limits for some numeric fields are defined as setup-driven/configurable but exact ranges are not included in the SRS. Please share min/max limits for full boundary coverage.

## Assumptions Used

- Test cases were generated only for common/generic screens, fields, workflows, roles, and integrations.
- Any field/validation explicitly tied to KCC, KSY, Animal Husbandry, or Fisheries was excluded.
- Where exact threshold values were not provided, boundary scenarios are written as configurable-limit validations.
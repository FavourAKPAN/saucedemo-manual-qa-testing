# Test Execution Report

## Project Information

**Project:** SauceDemo Manual QA Testing  
**Testing Type:** Manual Functional Testing  
**Environment:** Chrome / Android 14

## Execution Results

| Test Case | Area | Result |
|---|---|---|
| TC-001 | Login | PASS |
| TC-002 | Login | PASS |
| TC-003 | Login | FAIL |
| TC-004 | Login | FAIL |
| TC-005 | Login | PASS |
| TC-006 | Login | PASS |
| TC-007 | Login | FAIL / INCONCLUSIVE |
| TC-008 | Cart | PASS |
| TC-009 | Cart | PASS |
| TC-010 | Cart | PASS |
| TC-011 | Cart | PASS / OBSERVATION |
| TC-012 | Cart | PASS |
| TC-013 | Checkout | PASS |
| TC-014 | Checkout | PASS |
| TC-015 | Checkout | PASS |
| TC-016 | Checkout | PASS |

## Result Summary

**Total unique test cases executed:** 16

| Result | Count | Percentage |
|---|---:|---:|
| PASS | 13 | 81.25% |
| FAIL | 2 | 12.50% |
| FAIL / INCONCLUSIVE | 1 | 6.25% |
| **Total** | **16** | **100%** |

## Failed Tests

### TC-003 — Empty Username and Password
Login did not proceed, but no validation or error message was displayed.

**Related defect:** BU-001

### TC-004 — Valid Username With Empty Password
Login did not proceed, but no validation or error message was displayed.

**Related defect:** BU-002

## Inconclusive Test

### TC-007 — Very Long Password
The login attempt was rejected and an incorrect email/password message was displayed. The test was classified as inconclusive because the expected password-length behaviour was not based on an established requirement.

## Observation

### TC-011 — Invalid Cart Quantity
Invalid input did not cause incorrect cart calculations. Non-numeric input did not produce an explicit validation message, so this was recorded as an observation rather than a confirmed defect.

## Confirmed Defects

- BU-001 — Empty Login Fields Provide No Validation Feedback
- BU-002 — Empty Password Field Provides No Validation Feedback

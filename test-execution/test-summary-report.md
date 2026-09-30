# Test Summary Report

## Project Information

**Project:** SauceDemo Manual QA Testing  
**Testing Type:** Manual Functional Testing  
**Environment:** Chrome / Android 14

## Testing Objective

Evaluate key e-commerce workflows and identify functional or validation issues through manual testing.

## Areas Tested

- Login
- Product
- Cart
- Checkout

## Test Execution Summary

A total of **16 unique test cases** were executed.

| Result | Count | Percentage |
|---|---:|---:|
| PASS | 13 | 81.25% |
| FAIL | 2 | 12.50% |
| FAIL / INCONCLUSIVE | 1 | 6.25% |
| **Total** | **16** | **100%** |

## Key Findings

### Login
Most invalid login scenarios were handled correctly. However, validation feedback was missing when both login fields were empty or when the password was empty.

These resulted in:
- BU-001
- BU-002

### Product and Cart
Products could be added to the cart, quantities could be updated, and cart totals were updated correctly. Invalid quantity input did not cause incorrect calculations.

### Checkout
Required-field validation prevented incomplete submissions, and valid payment information resulted in successful order completion and an order confirmation page.

## Confirmed Defects

### BU-001
**Severity:** Low  
**Priority:** Medium  
**Status:** Open

No validation feedback was displayed when both login fields were empty.

### BU-002
**Severity:** Low  
**Priority:** Medium  
**Status:** Open

No validation feedback was displayed when a valid username was entered without a password.

## Inconclusive Result

### TC-007 — Very Long Password
The expected password-length validation behaviour was not based on an established requirement, so this was not classified as a confirmed defect.

## Testing Limitations

This cycle focused on manual functional testing using Chrome on Android 14. It did not cover performance, security, API, automation, accessibility compliance, or broad cross-browser/device testing.

## Conclusion

The majority of tested functionality behaved as expected. Two confirmed low-severity defects were identified in login validation. Further testing and retesting would be appropriate after fixes are implemented.

**Testing Status:** Completed  
**Unique Test Cases:** 16  
**Confirmed Defects:** 2  
**Inconclusive Results:** 1

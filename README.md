# SauceDemo Manual QA Testing

## Project Overview

This project demonstrates a manual functional testing process carried out on **SauceDemo**, an e-commerce web application.

The objective was to validate key user flows, identify functional issues, document test results, and report confirmed defects using structured QA practices.

The project covers the testing process from **test planning and scenario identification to test execution, defect reporting, and test summarisation**.

## Application Under Test

**Application:** SauceDemo  
**Application Type:** E-commerce web application  
**Testing Type:** Manual Functional Testing

## Testing Objectives

- Verify key e-commerce functionality.
- Validate behaviour with valid and invalid inputs.
- Identify functional and validation issues.
- Document actual results against expected results.
- Classify and report confirmed defects.
- Practise structured manual QA documentation.

## Testing Scope

### Login
- Invalid credentials
- Empty fields
- Missing password
- Invalid email/username format
- Very long password

### Product & Cart
- Product information
- Adding products to cart
- Adding the same product multiple times
- Cart quantity updates
- Cart total updates
- Invalid quantity input
- Zero quantity behaviour

### Checkout
- Required-field validation
- Missing city validation
- Successful payment
- Order confirmation
- Continue Shopping

## Test Environment

| Environment | Details |
|---|---|
| Device | Android |
| Operating System | Android 14 |
| Browser | Google Chrome |
| Testing Type | Manual |
| Test Data | Application-provided and controlled test data |

## Test Execution Summary

A total of **16 unique test cases** were executed.

| Result | Count | Percentage |
|---|---:|---:|
| PASS | 13 | 81.25% |
| FAIL | 2 | 12.50% |
| FAIL / INCONCLUSIVE | 1 | 6.25% |
| **Total** | **16** | **100%** |

> One previously documented test case was identified as a duplicate and removed from the final test count.

## Key Findings

### Login

Most invalid login scenarios were handled correctly. However, validation feedback was not displayed when required login information was left empty.

Two confirmed defects were identified:

- **BU-001:** No validation message when both login fields are empty.
- **BU-002:** No validation message when the password field is empty.

### Product & Cart

Products could be added to the cart, the cart count updated correctly, and adding the same product again increased its quantity. Quantity changes also updated the cart total correctly.

### Checkout

Required-field validation prevented incomplete submissions. A valid test payment successfully completed checkout and displayed an order confirmation.

## Confirmed Defects

### BU-001 — Empty Login Fields Provide No Validation Feedback

**Severity:** Low  
**Priority:** Medium  
**Status:** Open

### BU-002 — Empty Password Field Provides No Validation Feedback

**Severity:** Low  
**Priority:** Medium  
**Status:** Open

## Inconclusive Result

### TC-008 — Very Long Password

The application rejected the login attempt and displayed an incorrect email/password message.

The expected password-length validation behaviour was not based on an established requirement, so this was documented as **FAIL / INCONCLUSIVE** rather than a confirmed defect.

## Testing Deliverables

- Test Plan
- Test Scenarios
- Test Cases
- Test Execution Report
- Test Summary Report
- Bug Reports
- Testing Evidence/Screenshots

## Project Structure

```text
saucedemo-manual-qa-testing/
├── README.md
├── test-plan/
│   └── test-plan.md
├── test-scenarios/
│   └── test-scenarios.md
├── test-cases/
│   └── test-cases.md
├── test-execution/
│   ├── test-execution-report.md
│   └── test-summary-report.md
├── bug-reports/
│   ├── BU-001-empty-login-fields.md
│   └── BU-002-empty-password.md
└── screenshots/
    ├── login/
    ├── cart/
    └── checkout/
```

## Skills Demonstrated

- Manual Functional Testing
- Test Scenario Design
- Test Case Design
- Test Execution
- Positive & Negative Testing
- Validation Testing
- Defect Identification
- Bug Reporting
- Severity & Priority Classification
- Test Documentation
- QA Reporting
- Requirement-Based Testing

## Conclusion

This project provided practical experience in manually testing an e-commerce application through structured QA processes.

The testing involved creating test scenarios and test cases, executing them against the application, documenting actual results, identifying confirmed defects, and producing structured QA reports.

It also reinforced the importance of requirement-based testing, controlled test data, accurate defect classification, and separating confirmed defects from observations or inconclusive results.

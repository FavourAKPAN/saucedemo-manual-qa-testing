# BU-001 — Empty Login Fields Provide No Validation Feedback

**Bug ID:** BU-001  
**Module:** Login  
**Environment:** Chrome / Android 14  
**Severity:** Low  
**Priority:** Medium  
**Status:** Open

## Description

No validation message is displayed when the Login button is clicked with both Username and Password fields empty.

## Preconditions

User is on the SauceDemo login page.

## Steps to Reproduce

1. Leave Username empty.
2. Leave Password empty.
3. Click Login.

## Expected Result

Login should not proceed and appropriate validation feedback should be displayed.

## Actual Result

The user remains on the login page, but no validation or error message is displayed.

## Impact

Users who submit the login form without credentials receive no explanation of why the attempt did not proceed.

## Evidence

Add screenshot as:

`screenshots/login/BU-001.png`

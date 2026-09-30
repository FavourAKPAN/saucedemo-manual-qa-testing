# BU-002 — Empty Password Field Provides No Validation Feedback

**Bug ID:** BU-002  
**Module:** Login  
**Environment:** Chrome / Android 14  
**Severity:** Low  
**Priority:** Medium  
**Status:** Open

## Description

No validation message is displayed when a valid username is entered while the Password field is empty.

## Preconditions

User is on the SauceDemo login page.

## Steps to Reproduce

1. Enter a valid username.
2. Leave Password empty.
3. Click Login.

## Expected Result

Login should not proceed and an appropriate validation message should indicate that Password is required.

## Actual Result

The user remains on the login page, but no validation or error message is displayed.

## Impact

Users who forget to enter a password do not receive feedback explaining which required field needs attention.

## Evidence

Add screenshot as:

`screenshots/login/BU-002.png`

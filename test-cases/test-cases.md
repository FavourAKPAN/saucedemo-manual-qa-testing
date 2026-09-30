# Test Cases

## Login

### TC-001 — Verify Login Button
**Precondition:** User is on the login page.

**Steps:**
1. Open the login page.
2. Observe the Login button.

**Expected:** Login button is visible and accessible.

**Status:** PASS

### TC-002 — Login With Incorrect Password
**Precondition:** User is on the login page.

**Test Data:** Valid username and incorrect password.

**Steps:**
1. Enter valid username.
2. Enter incorrect password.
3. Click Login.

**Expected:** Login fails and appropriate error feedback is displayed.

**Actual:** Red error message displayed; user remained on login page and fields were cleared.

**Status:** PASS

### TC-003 — Empty Username and Password
**Precondition:** User is on the login page.

**Steps:**
1. Leave Username empty.
2. Leave Password empty.
3. Click Login.

**Expected:** Login does not proceed and validation feedback is displayed.

**Actual:** Page remained on login screen and no validation message was displayed.

**Status:** FAIL

### TC-004 — Valid Username With Empty Password
**Precondition:** User is on the login page.

**Test Data:** Valid username and empty password.

**Steps:**
1. Enter valid username.
2. Leave Password empty.
3. Click Login.

**Expected:** Login does not proceed and password validation feedback is displayed.

**Actual:** Page remained on login screen and no validation message was displayed.

**Status:** FAIL

### TC-005 — Empty Username With Valid Password
**Precondition:** User is on the login page.

**Test Data:** Empty username and valid password.

**Steps:**
1. Leave Username empty.
2. Enter valid password.
3. Click Login.

**Expected:** Login fails and appropriate error feedback is displayed.

**Actual:** Login failed and an error message was displayed. Password field was cleared.

**Status:** PASS

### TC-006 — Invalid Username/Email Format
**Precondition:** User is on the login page.

**Test Data:** Invalid email/username format.

**Steps:**
1. Enter invalid email/username format.
2. Enter a password.
3. Click Login.

**Expected:** Login does not proceed and appropriate validation feedback is displayed.

**Actual:** Error message indicated that the email format was incorrect. Login did not proceed.

**Status:** PASS

### TC-007 — Very Long Password
**Precondition:** User is on the login page.

**Test Data:** Valid username and very long password.

**Steps:**
1. Enter valid username.
2. Enter very long password.
3. Click Login.

**Expected:** System handles a password exceeding the accepted length according to the defined password-length requirement.

**Actual:** Incorrect email/password error was displayed and login did not proceed.

**Status:** FAIL / INCONCLUSIVE

**Note:** A maximum password-length requirement was not established, so this was not reported as a confirmed defect.

## Product & Cart

### TC-008 — Add Product to Cart
**Precondition:** Product details page is open and cart is empty.

**Steps:**
1. Select a product.
2. Click Add to Cart.
3. Observe cart badge.
4. Open cart.

**Expected:** Product is added and cart count updates.

**Actual:** Button changed state, cart badge updated, and product appeared in cart.

**Status:** PASS

### TC-009 — Add Same Product Multiple Times
**Precondition:** Product is already in cart.

**Steps:**
1. Return to the product.
2. Add the same product again.
3. Open cart.
4. Check quantity.

**Expected:** Quantity reflects the additional product.

**Actual:** Cart badge increased to 2 and product quantity increased to 2.

**Status:** PASS

### TC-010 — Update Cart Quantity
**Precondition:** Product is in cart.

**Steps:**
1. Change quantity.
2. Click Update.
3. Observe cart total.

**Expected:** Quantity and total update correctly.

**Actual:** Quantity and total updated correctly.

**Status:** PASS

### TC-011 — Invalid Cart Quantity
**Precondition:** Product is in cart.

**Steps:**
1. Enter an invalid quantity.
2. Click Update.
3. Observe quantity and total.

**Expected:** Invalid input does not cause incorrect calculations or unintended behaviour.

**Actual:** Invalid input was rejected/restored and did not result in an incorrect cart total. Non-numeric input did not display a validation message.

**Status:** PASS / OBSERVATION

### TC-012 — Quantity of Zero
**Precondition:** Product is in cart.

**Steps:**
1. Change quantity to 0.
2. Click Update.
3. Observe cart.

**Expected:** Zero quantity is handled consistently.

**Actual:** Product was removed, cart badge became 0, and cart total became 0.

**Status:** PASS

## Checkout

### TC-013 — Checkout With Empty Required Fields
**Precondition:** Product is in cart and checkout page is open.

**Steps:**
1. Leave required fields empty.
2. Click Pay Now.
3. Observe form.

**Expected:** Payment does not proceed and validation messages are displayed.

**Actual:** Required fields were highlighted in red and validation messages were displayed. Payment did not proceed.

**Status:** PASS

### TC-014 — Missing City
**Precondition:** Checkout page is open.

**Steps:**
1. Complete all required fields except City.
2. Leave City empty.
3. Click Pay Now.

**Expected:** Payment does not proceed and City displays validation feedback.

**Actual:** Page scrolled to City, which was highlighted in red with a validation message.

**Status:** PASS

### TC-015 — Successful Checkout
**Precondition:** Product is in cart.

**Test Data:** Valid checkout information and provided valid test card.

**Steps:**
1. Enter valid contact information.
2. Enter delivery information.
3. Select shipping method.
4. Enter valid payment information.
5. Click Pay Now.

**Expected:** Payment succeeds and order confirmation is displayed.

**Actual:** Payment succeeded and an order confirmation page displayed order details.

**Status:** PASS

### TC-016 — Continue Shopping
**Precondition:** Order has been successfully completed.

**Steps:**
1. Click Continue Shopping.
2. Observe resulting page.

**Expected:** User returns to the shopping experience.

**Actual:** User returned to the home/shopping page. Cart was empty and products were visible.

**Status:** PASS

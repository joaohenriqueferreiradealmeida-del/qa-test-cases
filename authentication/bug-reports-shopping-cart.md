**Bug Reports – Shopping Cart**

**Objective:**
Identify functional, validation, calculation, and usability defects in the shopping cart flow, ensuring correct product handling, accurate pricing, reliable checkout behavior, and a smooth user experience.

**Scope:**
These bug reports cover issues related to:
- Adding and removing products from the cart
- Updating product quantity
- Price and total value calculations
- Cart persistence and state management
- Checkout flow validation (before payment)
- Address validation during purchase process

**Out of Scope:**
- Payment gateway processing (external providers)
- Order fulfillment and delivery tracking
- Post-purchase flows (refunds, cancellations, invoices)

**Test Environment:**
- Application Type: Web E-commerce Platform
- Module: Shopping Cart / Checkout
- Browser: Google Chrome
- Operating System: Windows / Android
- Environment: Test / Staging

**Preconditions:**
- System is online and accessible
- User is registered and logged in
- At least one product is available for purchase
- Shopping cart functionality is enabled

**Test Type:**
- Manual Testing
- Functional Testing
- Validation Testing
- Exploratory Testing

---

**BUG-CART-01 – Cart does not update product quantity**

**Description:**
The cart does not correctly update product quantity when increased.

**Steps:**
1. Log in
2. Add product to cart
3. Increase quantity

**Expected Result:**
- Quantity updates correctly

**Actual Result:**
- Quantity remains unchanged

**Severity:** Medium
**Priority:** Medium
**Status:** Open

---

**BUG-CART-02 – Removed product remains in purchase summary**

**Description:**
- Removed items still appear in purchase summary.

**Steps:**
1. Add product
2. Proceed to checkout
3. Cancel and remove product

**Expected Result:**
- Product removed completely

**Actual Result:**
- Product still visible

**Severity:** Low
**Priority:** Low
**Status:** Open

--- 

**BUG-CART-03 – Total value not updated after quantity change**

**Description:**
Total price does not update after quantity change.

**Expected Result:**
Total reflects correct quantity

**Actual Result:**
- Total remains for one unit

**Severity:** Medium
**Priority:** Medium
**Status:** Open

---

**BUG-CART-04 – Checkout allows purchase without products**

**Description:**
- Checkout proceeds even with empty cart.

**Expected Result:**
- System blocks checkout

**Actual Result:**
- Checkout allowed

**Severity:** Medium
**Priority:** Medium
**Status:** Open

---

**BUG-CART-05 – Address validation is not enforced**

**Description:**
- Checkout proceeds with invalid address.

**Severity:** High
**Priority:** High
**Status:** Open

---

**BUG-CART-06 – Duplicate payment allowed**

**Description:**
- System allows multiple payments for same order.

**Expected Result:**
- Duplicate payments blocked

**Actual Result:**
- Multiple charges allowed

**Severity:** High
**Priority:** High
**Status:** Open

---

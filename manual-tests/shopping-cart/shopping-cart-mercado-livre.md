**Test Cases – Shopping Cart (Visualization & Editing)**

**Objective:**
Validate the visualization, update, and removal of products in the shopping cart of an e-commerce platform, ensuring correct price updates and cart behavior during user interactions.

**Scope:**
These test cases cover:
- Adding products to the cart
- Updating product quantities
- Price recalculation
- Removing and restoring products
- Navigation during the checkout flow

**Preconditions:**
- User has a valid account
- User is logged in
- E-commerce platform is online and accessible
- At least one product available for purchase

**Test Environment**
- Platform: Mercado Livre (Web)
- Browser: Desktop (Web)
- Authentication: Google account login

---

**Test Case**

**TC-CART-01 – View and edit product in shopping cart**

**Description:**
Verify that a logged-in user can add a product to the cart, update quantities, observe price changes, remove the product, and restore it successfully.

**Steps:**
1. Access the e-commerce platform
2. Log in with a valid user account
3. Select a product
4. Add the product to the shopping cart
5. Increase the product quantity
6. Decrease the product quantity
7. Observe price updates after each change
8. Remove the product from the cart
9. Use the “Undo removal” option
10. Click on “Continue shopping”
11. Return to the cart
12. Navigate to the “Mercado Livre Full” section

**Test Data:**
- Product: Headphones
- Login method: Google account

**Expected Result:**
- Product can be added to the cart successfully
- Quantity changes are applied correctly
- Total price updates according to quantity changes
- Product can be removed and restored using the undo option
- No errors occur during navigation or cart updates

**Actual Result:** The cart behaved as expected.
The product was successfully added, updated, removed, and restored.
Price updates occurred correctly after each quantity change.
The “Undo removal” feature worked properly, and no errors were identified during the tested flow.

**Status:** PASS

---

**Additional Observations**
- Price updates occur quickly, with no noticeable delay
- User experience remains smooth during cart interactions

**Extra Steps Performed**
- Multiple quantity changes (increase and decrease)
- Validation of total price recalculation
- Removal and restoration of product
- Navigation to checkout and back to the cart
- Access to the Mercado Livre Full section

**Evidence:**
- Video recording demonstrating:
- User login
- Product selection
- Cart interactions
- Quantity updates
- Removal and restoration flow

---

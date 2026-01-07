Shopping Cart – Test Cases

Objective
Validate the shopping cart and checkout functionality, ensuring correct behavior for product availability, quantity rules, and purchase flow.

Scope
These test cases cover functional, business rule, and negative scenarios related to cart management and checkout in an e-commerce system.

Preconditions
- Application is online and accessible
- User is on the product listing page
- Payment gateway is available

---

Test Cases

TC-CART-01 – Complete purchase with product in stock

Steps:
1. Access the product listing page
2. Select an available product
3. Add product to cart
4. Proceed to checkout
5. Enter valid payment and shipping data
6. Confirm purchase

Expected Result:
- Product is successfully purchased
- Payment is authorized
- Order is completed
- Shipping information is displayed

---

TC-CART-02 – Attempt purchase with product out of stock

Steps:
1. Access the product listing page
2. Select a product with no stock available
3. Proceed to checkout

Expected Result:
- System displays an “Out of stock” message
- Purchase is blocked
- User is prompted to select another product

---

TC-CART-03 – Update quantity greater than available stock

Steps:
1. Add a product to the cart
2. Update quantity to a value greater than available stock

Expected Result:
- System prevents quantity update
- Validation message is displayed informing stock limit

---

TC-CART-04 – Product becomes unavailable after payment (Critical Bug)

Steps:
1. Add available product to cart
2. Proceed to checkout
3. Complete payment
4. Finalize purchase

Expected Result:
- System validates stock before confirming order
- Purchase is canceled or adjusted if product becomes unavailable
- User is notified clearly

Actual Result:
- Payment is processed
- System incorrectly confirms purchase
- Product is unavailable
❌ Defect identified

---

TC-CART-05 – Add product to cart

Steps:
1. Access product listing
2. Select a product
3. Click “Add to cart”

Expected Result:
- Product is added to cart
- Cart is updated with correct quantity and price

---

TC-CART-06 – Remove product from cart

Steps:
1. Add a product to the cart
2. Remove the product from the cart

Expected Result:
- Product is removed successfully
- Cart updates correctly
- Product availability is restored if applicable

---

Notes
- Stock validation is a critical business rule
- Payment confirmation must always revalidate product availability
- Identified defects should be logged as bug reports

---

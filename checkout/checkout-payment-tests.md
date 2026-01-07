Checkout & Payment – Test Cases

Objective
Validate the checkout and credit card payment process, ensuring that transactions are processed correctly, invalid data is rejected, and proper error handling is applied in failure scenarios.

Scope
These test cases cover functional, negative, and exception scenarios related to credit card payments during checkout.

Preconditions
- User is logged in
- Product is available for purchase
- Product is added to the cart
- Checkout page is accessible
- Payment gateway is available (except where stated)

---

Test Cases

TC-CHECKOUT-01 – Payment with invalid card number format

Steps:
1. Access the application
2. Login with a valid user
3. Add a product to the cart
4. Proceed to checkout
5. Select Credit Card as payment method
6. Enter an invalid card number format
7. Confirm payment

Expected Result:
- Payment is rejected
- System displays an error message indicating invalid card data
- User remains on checkout page
- Order is not completed

---

TC-CHECKOUT-02 – Payment with expired credit card

Steps:
1. Login to the application
2. Add a product to the cart
3. Proceed to checkout
4. Select Credit Card as payment method
5. Enter expired card details
6. Confirm payment

Expected Result:
- Transaction is blocked
- System displays a message indicating expired or invalid card
- Order status remains as Payment Not Approved or Cancelled
- Purchase is not completed

---

TC-CHECKOUT-03 – Payment refused by card issuer

Steps:
1. Login to the application
2. Add a product to the cart
3. Proceed to checkout
4. Select Credit Card as payment method
5. Enter valid card data
6. Confirm payment

Expected Result:
- Payment is refused by the bank
- System displays a clear message such as “Payment not authorized by the bank”
- Order does not move to approved or shipping status
- User is allowed to choose another payment method

---

TC-CHECKOUT-04 – Payment with blocked or insufficient limit card

Steps:
1. Login to the application
2. Add a product to the cart
3. Proceed to checkout
4. Select Credit Card as payment method
5. Enter card data with no available limit or blocked status
6. Confirm payment

Expected Result:
- Payment is rejected
- System displays message indicating insufficient limit or blocked card
- Order is not completed
- User can retry payment with another card

---

TC-CHECKOUT-05 – Payment with invalid CVV

Steps:
1. Login to the application
2. Add a product to the cart
3. Proceed to checkout
4. Select Credit Card as payment method
5. Enter invalid CVV
6. Confirm payment

Expected Result:
- System highlights CVV field as invalid
- Error message is displayed
- Payment is not processed
- Order does not advance to shipping or approval status

---

TC-CHECKOUT-06 – Payment gateway instability or timeout

Steps:
1. Login to the application
2. Add a product to the cart
3. Proceed to checkout
4. Select Credit Card as payment method
5. Confirm payment
6. Simulate payment gateway timeout or technical error

Expected Result:
- System displays a friendly error message informing temporary instability
- User is not charged
- Order is not duplicated
- User remains logged in and can retry payment
- Cart items are preserved

---

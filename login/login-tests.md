# Test Cases – Login

## Objective
Validate the login functionality to ensure that only registered users with valid credentials can access the system, and that appropriate error messages are displayed for invalid scenarios.

## Scope
These test cases cover functional, negative, and validation scenarios related to the user login feature.

## Preconditions
- User is on the login page
- System is online and accessible
- User account exists in the system (when applicable)

---

## Test Cases

TC-LOGIN-01 – Login with valid email and valid password

Type: Positive Flow

Preconditions:
- User is on login page
- User is registered
  
Steps:
1. Enter a valid email
2. Enter a valid password
3. Click the "Login" button
   
Test Data:
- Email: user@example.com
- Password: ValidPassword123
  
Expected Result:
User is successfully authenticated and redirected to the dashboard.

Status: Not Executed

---

TC-LOGIN-02 – Login with invalid email format

Type: Negative Flow

Steps:
1. Enter an invalid email format (without "@")
2. Enter a valid password
3. Click the "Login" button
   
Expected Result:
System displays validation message: "Invalid email format" and login is blocked.

Status: Not Executed

---

TC-LOGIN-03 – Login with valid email and invalid password

Type: Security Validation

Steps:
1. Enter a valid email
2. Enter an incorrect password
3. Click the "Login" button

Expected Result:
System denies access and displays authentication error message.

Status: Not Executed

---

TC-LOGIN-04 – Login with empty password field

Type: Constraint Validation

Steps:
1. Enter a valid email
2. Leave password field empty
3. Click the "Login" button

Expected Result:
System displays required field validation message.

Status: Not Executed

---

TC-LOGIN-05 – Login with non-registered email

Type: Business Rule

Steps:
1. Enter a non-registered email
2. Enter any password
3. Click the "Login" button

Expected Result:
System displays error message indicating user not found.

Status: Not Executed

---

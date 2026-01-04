# Login – Test Cases

## Objective
Validate the login functionality to ensure that only registered users with valid credentials can access the system, and that proper error messages are displayed for invalid scenarios.

## Scope
These test cases cover functional and negative scenarios related to the user login feature.

## Preconditions
- User is on the login page
- System is online and accessible
- User account exists in the system (when applicable)

---

## Test Cases

### TC-LOGIN-01 – Login with valid email and valid password
**Steps:**
1. Enter a valid email
2. Enter a valid password
3. Click the "Login" button

**Expected Result:**
- User is successfully logged in
- User is redirected to the dashboard

---

### TC-LOGIN-02 – Login with invalid email format
**Steps:**
1. Enter an email without "@"
2. Enter a valid password
3. Click the "Login" button

**Expected Result:**
- System displays an error message indicating invalid email format
- User is not logged in

---

### TC-LOGIN-03 – Login with valid email and invalid password
**Steps:**
1. Enter a valid email
2. Enter an incorrect password
3. Click the "Login" button

**Expected Result:**
- System displays an authentication error message
- User is not logged in

---

### TC-LOGIN-04 – Login with empty password field
**Steps:**
1. Enter a valid email
2. Leave the password field empty
3. Click the "Login" button

**Expected Result:**
- System displays a required field validation message
- User is not logged in

---

### TC-LOGIN-05 – Login with non-registered email
**Steps:**
1. Enter an email not registered in the system
2. Enter any password
3. Click the "Login" button

**Expected Result:**
- System displays a message indicating user not found
- User is not logged in

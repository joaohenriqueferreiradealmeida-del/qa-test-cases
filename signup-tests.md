# Sign Up – Test Cases

## Objective
Validate the user registration functionality, ensuring that new users can register successfully with valid data and that the system properly handles invalid inputs and business rules.

## Scope
These test cases cover functional and negative scenarios related to user registration (sign up).

## Preconditions
- User is on the registration page
- System is online and accessible

---

## Test Cases

### TC-SIGNUP-01 – Registration with valid data
**Steps:**
1. Enter a valid name
2. Enter a valid email
3. Enter a valid password
4. Confirm the same password
5. Click the "Sign Up" button

**Expected Result:**
- User account is created successfully
- User receives a confirmation message or is redirected to login/dashboard

---

### TC-SIGNUP-02 – Registration with already registered email
**Steps:**
1. Enter a valid name
2. Enter an email already registered in the system
3. Enter a valid password
4. Confirm the same password
5. Click the "Sign Up" button

**Expected Result:**
- System displays a message indicating the email is already registered
- Account is not created

---

### TC-SIGNUP-03 – Registration with weak password
**Steps:**
1. Enter a valid name
2. Enter a valid email
3. Enter a weak or short password
4. Confirm the same password
5. Click the "Sign Up" button

**Expected Result:**
- System displays a password strength validation message
- Account is not created

---

### TC-SIGNUP-04 – Registration with mismatched passwords
**Steps:**
1. Enter a valid name
2. Enter a valid email
3. Enter a password
4. Enter a different password in confirmation
5. Click the "Sign Up" button

**Expected Result:**
- System displays a message indicating passwords do not match
- Account is not created

---

### TC-SIGNUP-05 – Registration with invalid email format
**Steps:**
1. Enter a valid name
2. Enter an email without "@" or domain
3. Enter a valid password
4. Confirm the same password
5. Click the "Sign Up" button

**Expected Result:**
- System displays an invalid email format message
- Account is not created

---

### TC-SIGNUP-06 – Registration with empty required fields
**Steps:**
1. Leave one or more required fields empty
2. Click the "Sign Up" button

**Expected Result:**
- System displays required field validation messages
- Account is not created

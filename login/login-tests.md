# Test Cases - Login

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

{
  "id": "TC-LOGIN-01",
  "type": "Positive Flow",
  "expected_result": "Success",
  "status_code": 200,
  "action": "User redirected to dashboard"
}

---

### TC-LOGIN-02 – Login with invalid email format
**Steps:**
1. Enter an email without "@"
2. Enter a valid password
3. Click the "Login" button

{
  "id": "TC-LOGIN-02",
  "type": "Negative Flow",
  "input_error": "Malformed Email",
  "expected_result": "Validation Error: 'Invalid email format'",
  "status": "FAIL"
}

---

### TC-LOGIN-03 – Login with valid email and invalid password
**Steps:**
1. Enter a valid email
2. Enter an incorrect password
3. Click the "Login" button

{
  "id": "TC-LOGIN-03",
  "type": "Security Validation",
  "expected_result": "Authentication Error",
  "status_code": 401,
  "status": "FAIL"
}

---

### TC-LOGIN-04 – Login with empty password field
**Steps:**
1. Enter a valid email
2. Leave the password field empty
3. Click the "Login" button

{
  "id": "TC-LOGIN-04",
  "type": "Constraint Validation",
  "expected_result": "Required field message displayed",
  "status": "FAIL"
}

---

### TC-LOGIN-05 – Login with non-registered email
**Steps:**
1. Enter an email not registered in the system
2. Enter any password
3. Click the "Login" button

{
  "id": "TC-LOGIN-05",
  "type": "Business Rule",
  "expected_result": "User not found error",
  "status_code": 404,
  "status": "FAIL"
}

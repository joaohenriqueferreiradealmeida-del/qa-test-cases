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

{
  "id": "TC-SIGNUP-01",
  "type": "Positive Flow",
  "expected_result": "Account created successfully",
  "http_status_expected": 201,
  "status": "PASS"
}
---

### TC-SIGNUP-02 – Registration with already registered email
**Steps:**
1. Enter a valid name
2. Enter an email already registered in the system
3. Enter a valid password
4. Confirm the same password
5. Click the "Sign Up" button

{
  "id": "TC-SIGNUP-02",
  "type": "Business Rule Validation",
  "conflict_field": "email",
  "expected_result": "Error: 'Email already registered'",
  "status_code": 409,
  "status": "FAIL"
}
---

### TC-SIGNUP-03 – Registration with weak password
**Steps:**
1. Enter a valid name
2. Enter a valid email
3. Enter a weak or short password
4. Confirm the same password
5. Click the "Sign Up" button

{
  "id": "TC-SIGNUP-03",
  "type": "Security Constraint",
  "rule": "min_length: 8",
  "expected_result": "System rejects weak password",
  "status": "FAIL"
}
---

### TC-SIGNUP-04 – Registration with mismatched passwords
**Steps:**
1. Enter a valid name
2. Enter a valid email
3. Enter a password
4. Enter a different password in confirmation
5. Click the "Sign Up" button

{
  "id": "TC-SIGNUP-04",
  "type": "Data Integrity",
  "validation": "password_confirmation",
  "expected_result": "Error: 'Passwords do not match'",
  "status": "PASS"
}
---

### TC-SIGNUP-05 – Registration with invalid email format
**Steps:**
1. Enter a valid name
2. Enter an email without "@" or domain
3. Enter a valid password
4. Confirm the same password
5. Click the "Sign Up" button

{
  "id": "TC-SIGNUP-05",
  "type": "Negative Flow",
  "expected_result": "Invalid email format message",
  "status_code": 400,
  "status": "FAIL"
}
---

### TC-SIGNUP-06 – Registration with empty required fields
**Steps:**
1. Leave one or more required fields empty
2. Click the "Sign Up" button

{
  "id": "TC-SIGNUP-06",
  "type": "Field Validation",
  "fields": ["name", "email", "password"],
  "expected_result": "Required field messages displayed",
  "status": "FAIL"
}

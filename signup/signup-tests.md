Test Cases – Sign Up (User Registration)

Objective
Validate the user registration functionality to ensure that new users can successfully create an account using valid data, and that the system correctly handles validation errors, business rules, and invalid inputs.

Scope
These test cases cover positive, negative, and validation scenarios related to the user registration (sign up) feature.

Preconditions
- User is on the registration (sign up) page
- System is online and accessible
- User is not authenticated

---

Test Cases

TC-SIGNUP-01 – Registration with valid data

Steps:
1. Enter a valid name
2. Enter a valid email
3. Enter a valid password
4. Confirm the same password
5. Click the "Sign Up" button

Expected Result:
The system creates the account successfully and redirects the user to the login page or dashboard.

---

TC-SIGNUP-02 – Registration with already registered email

Steps:
1. Enter a valid name
2. Enter an email already registered in the system
3. Enter a valid password
4. Confirm the same password
5. Click the "Sign Up" button

Expected Result:
The system displays an error message informing that the email is already registered.

---

TC-SIGNUP-03 – Registration with weak password

Steps:
1. Enter a valid name
2. Enter a valid email
3. Enter a weak or short password
4. Confirm the same password
5. Click the "Sign Up" button

Expected Result:
The system rejects the password and displays a message indicating password strength requirements.

---

TC-SIGNUP-04 – Registration with mismatched passwords

Steps:
1. Enter a valid name
2. Enter a valid email
3. Enter a password
4. Enter a different password in the confirmation field
5. Click the "Sign Up" button

Expected Result:
The system displays an error message indicating that the passwords do not match.

---

TC-SIGNUP-05 – Registration with invalid email format

Steps:
1. Enter a valid name
2. Enter an email with an invalid format (missing "@" or domain)
3. Enter a valid password
4. Confirm the same password
5. Click the "Sign Up" button

Expected Result:
The system displays a validation message indicating an invalid email format.

---

TC-SIGNUP-06 – Registration with empty required fields

Steps:
1. Leave one or more required fields empty
2. Click the "Sign Up" button

Expected Result:
The system displays validation messages indicating that required fields must be filled

---

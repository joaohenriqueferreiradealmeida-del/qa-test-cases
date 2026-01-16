**Authentication – Signup Bug Reports**

**Objective:**
Identify defects in the user registration process, focusing on data validation, business rules, and proper user feedback during account creation.

**Scope:**
These bug reports include:
- Email validation
- Password rules enforcement
- Password confirmation validation
- Duplicate account prevention

**Out of scope:**
- Login functionality
- Email verification flows

**Test Environment:**
- Application Type: Web Application
- Module: Authentication – Signup
- Browser: Google Chrome
- Operating System: Windows
- Environment: Test / Staging

**Preconditions:**
- System is online
- Signup page is accessible
- User is not authenticated

**Test Type:**
- Manual Testing
- Functional Testing
- Validation Testing

---

**BUG-SIGNUP-001 – Signup allows password below minimum length**

**Description:**
The registration form accepts passwords shorter than the minimum required length without displaying validation errors.

**Preconditions:**
- System is online
- Signup page is accessible

**Steps to Reproduce:**
1. Access signup page
2. Enter valid email
3. Enter password shorter than required minimum
4. Submit form

**Expected Result:**
- System blocks submission
- Validation message informs password length requirements

**Actual Result**
- Account is created successfully with weak password

**Severity:** High
**Priority:** High
**Status:** Open
**Attachments:** Screenshot showing successful signup

---

**BUG-SIGNUP-002 – Signup does not validate password confirmation mismatch**

**Description:**
The system allows user registration when the password and password confirmation fields contain different values.

**Preconditions:**
- System online
- Signup page accessible

**Steps to Reproduce:**
1. Access signup page
2. Enter valid email
3. Enter password
4. Enter a different password in confirmation field
5. Submit form

**Expected Result:**
- System blocks registration
- Error message indicates password mismatch

**Actual Result:**
Page freezes or account is created without validation

**Severity:** High
**Priority:** High
**Status:** Open
**Attachments:** Video showing form submission and page failure

---

**Bug Reports – Signup / User Registration**

**Objective:** Identify functional, validation and error handling failures in the user registration flow, ensuring security, data integrity and adequate feedback to the user.

**General preconditions:**
- Online and accessible system
- Registration page available
- User using supported browser

---

**BUG-SIGNUP-003 – System allows registration with an already registered email**

**Description:**
The system allows a new user to register using an email address that already exists in the database.

**Steps to Reproduce:**
1. Access the registration page
2. Enter an email already registered
3. Enter a valid password
4. Click on Register

**Expected Result:**
- Registration should be blocked
- Message indicating email already in use should be displayed

**Actual Result:**
- Registration is completed
- User is redirected to home page

**Severity:** Medium
**Priority:** Low
**Status:** Open

---

**BUG-SIGNUP-004 – Registration accepts password below minimum length**

**Description:**
The system allows account creation using passwords shorter than the minimum required length.

**Steps to Reproduce:**
1. Access registration page
2. Enter valid email
3. Enter password shorter than allowed
4. Submit form

**Expected Result:**
- Validation message about password length

**Actual Result:**
- Account is created successfully

**Severity:** High
**Priority:** High
**Status:** Open

**BUG-SIGNUP-005 – Password confirmation mismatch is not validated**

**Description:**
The system does not validate whether password and confirmation match.

**Steps to Reproduce:**
1. Access registration page
2. Enter valid data
3. Enter password
4. Enter different confirmation password
4. Submit form

**Expected Result:**
- Error message indicating mismatch

**Actual Result:**
- No validation message
- Page freezes or reloads blank

**Severity: Medium**
**Priority:** High
**Status:** Open

**BUG-SIGNUP-006 – Email field accepts invalid format**

**Description:**
Invalid email formats are accepted during registration.

**Steps to Reproduce:**
1. Access registration page
2. Enter invalid email format
3. Submit form

**Expected Result:**
- Invalid email format message

**Actual Result:**
- Registration proceeds

**Severity:** High
**Priority:** High
**Status:** Open

---

**BUG-SIGNUP-007 – System creates user with invalid data**

**Description:**
Mandatory fields are not properly validated during registration.

**Steps to Reproduce:**
1. Access registration page
2. Enter invalid data
3. Submit form

**Expected Result**
- Validation errors displayed

**Actual Result:**
- User account is created

**Severity:** High
**Priority:** High
**Status:** Open

---

**BUG-SIGNUP-008 – Technical error (500) exposed after registration**

**Description:**
The system exposes a technical error after form submission.

**Steps to Reproduce:**
1. Access registration page
2. Fill valid data
3. Submit form

**Expected Result:**
- User redirected to home page

**Actual Result:**
- 500 Internal Server Error displayed

**Severity:** High
**Priority:** High
**Status:** Open

---

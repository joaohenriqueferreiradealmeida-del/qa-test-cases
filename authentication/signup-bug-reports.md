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

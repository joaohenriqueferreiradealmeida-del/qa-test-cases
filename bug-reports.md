**# Bug Reports**

This document contains sample bug reports identified during manual testing
of authentication features (Login and Sign Up), simulating real-world QA activities.

---

**## BUG-LOGIN-01 – Login allows access with invalid password**

**Environment:**
- Application: Web App (Authentication Module)
- Browser: Google Chrome
- OS: Windows / Android
- Test Type: Manual

**Precondition:**
- User is registered in the system
- User is on the Login page

**Steps to Reproduce:**
1. Enter a valid registered email
2. Enter an invalid password
3. Click on the "Login" button

**Expected Result:**
- System should block access
- Error message should be displayed: "Invalid email or password"

**Actual Result:**
- User is redirected to the dashboard despite invalid credentials

**Severity:** High  
**Priority:** High  
**Status:** Open

---

**## BUG-LOGIN-02 - Login allows access with invalid password**

**Environment:**
- Web application
- Browser: Chrome

**Precondition**
- User is on teh login page
- User account exists in the system

**Steps to Reproduce**
1. Enter a valid registered email
2. Enter an invalid password
3. Click on the "Login" button

**Test Data:**
- Email: valid registered email
- Password: invalid password

**Expected Result:**
- System should block login
- Error message should be displayed indicating invalid credentials

**Actual Result:**
- System allows login with invalid password

**Status**
- Open

**Severity:**
- Critical

**Priority:**
- High

---

**Bug Reports – Authentication & User Management**
**Objective:**
Document critical defects related to authentication, user registration, session management, and input validation to improve system security, usability, and reliability.

**Scope:**
These bug reports focus on login, signup, password validation, session handling, and user feedback errors in a web application.

**Environment:**
- Application type: Web
- Browser: Google Chrome
- OS: Windows 10
- Environment: Staging / Test

---

**BUG-LOGIN-001 – Login allows access with invalid password**

**Description:**
When attempting to log in using a valid registered email and an invalid password, the system incorrectly grants access to the dashboard instead of blocking authentication.

**Preconditions:**
- System is online
- User account exists
- Login page is accessible

**Steps to Reproduce:**
1. Access the login page
2. Enter a valid registered email
3. Enter an invalid password
4. Click on Login

**Expected Result:**
- System blocks access
- Authentication error message is displayed
- Password recovery option is suggested

**Actual Result:**
- User is authenticated and redirected to the dashboard

**Severity:** Critical
**Priority:** High
**Status:** Open
**Attachments:** Screenshot and video showing access after invalid login

---

**BUG-LOGIN-002 – Login accepts non-existent email**

**Description:**
The system allows login attempts using an email that does not exist in the database, granting access or showing incorrect flows.

**Preconditions:**
- System is online
- Login page is accessible

**Steps to Reproduce:**
1. Access login page
2. Enter a non-registered email
3. Enter any password
4. Click Login

**Expected Result:** 
- System blocks access
- Error message indicating email not found is displayed

**Actual Result:**
- Login flow continues and access is granted or alternate login options are shown

**Severity:** Critical
**Priority:** High
**Status:** Open
**Attachments:** Screenshot and video

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

**BUG-SEC-001 – Account is not locked after multiple failed login attempts**

**Description:**
After multiple consecutive failed login attempts, the system does not block the user account, exposing it to brute-force attacks.

**Preconditions:**
- System online
- User account exists

**Steps to Reproduce:**
1. Attempt login with invalid credentials multiple times
2. Observe system behavior

**Expected Result:** 
- Account is temporarily locked
- Lockout message is displayed

**Actual Result:**
- Unlimited login attempts allowed

**Severity:** Critical
**Priority:** High
**Status:** Open
**Attachments:** Video showing repeated attempts

---

**BUG-SEC-002 – Session remains active after logout**

**Description:**
After logging out, the user session remains active and allows access to authenticated pages.

**Preconditions:**
- User is logged in
- System online

**Steps to Reproduce:**
1. Login
2. Navigate through the system
3. Click Logout
4. Use browser back button or direct URL

**Expected Result:**
- Session is terminated
- User is redirected to login page

**Actual Result:**
- User continues to access protected pages

**Severity:** Critical
**Priority:** Critical
**Status:** Open

---

**BUG-UX-001 – Technical error message displayed to end user**

**Description:**
When login fails, the system displays a technical error message (e.g., HTTP 500, NullPointerException) instead of a user-friendly message.

**Preconditions:**
- System online
- Login page accessible

**Steps to Reproduce:**
1. Attempt login with invalid credentials
2. Submit form

**Expected Result:**
- Friendly error message explaining authentication failure

**Actual Result:**
- Technical error message displayed

**Severity:** Medium
**Priority:** Low
**Status:** Open
**Attachments:** Screenshot

---

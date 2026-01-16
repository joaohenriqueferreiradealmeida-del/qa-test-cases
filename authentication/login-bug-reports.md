**Authentication – Login Bug Reports**

**Objective:**
Document and track defects related to the user login process, ensuring secure authentication, proper validation of credentials, and correct system behavior during access attempts.

**Scope:**
These bug reports cover scenarios involving:
- Credential validation (email and password)
- Access control
- Error handling during login
- Session initiation after authentication

**Out of scope:**
- Password recovery
- Account creation

**Test Environment:**
- Application Type: Web Application
- Module: Authentication – Login
- Browser: Google Chrome
- Operating System: Windows / Android
- Environment: Test / Staging

**Preconditions:**
- System is online and accessible
- User account exists in the system
- Login page is available

**Test Type:**
- Manual Testing
- Functional Testing
- Negative Scenarios
 
---

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

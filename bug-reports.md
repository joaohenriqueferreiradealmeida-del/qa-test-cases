# Bug Reports

This document contains sample bug reports identified during manual testing
of authentication features (Login and Sign Up), simulating real-world QA activities.

---

## BUG-LOGIN-01 – Login allows access with invalid password

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

## BUG-LOGIN-02 - Login allows access with invalid password

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

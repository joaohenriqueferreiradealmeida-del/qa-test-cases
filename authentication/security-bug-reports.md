**Security – Authentication & Session Bug Reports**

**Objective:**
Detect security-related vulnerabilities associated with authentication and session management that could expose the system to unauthorized access or misuse.

**Scope:**
These bug reports focus on:
- Session handling
- Logout behavior
- Protection against brute-force attacks
- Account security controls

**Out of scope:**
- Network security
- Encryption mechanisms

**Test Environment:**
- Application Type: Web Application
- Module: Authentication & Session Management
- Browser: Google Chrome
- Operating System: Windows
- Environment: Test / Staging

**Preconditions:**
- User account exists
- User is authenticated (when applicable)
- System is online

**Test Type:**
- Manual Testing
- Security Testing
- Exploratory Testing

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

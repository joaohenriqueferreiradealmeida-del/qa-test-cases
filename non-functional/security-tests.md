**Test Cases – Security (Non-Functional)**

**Objective:**
Validate system protection against common security vulnerabilities and ensure secure handling of authentication and user inputs.

**Scope:**
These test cases focus on authentication security, input validation, and access control based on OWASP fundamentals.

**Preconditions:**
- Application is accessible
- Test user accounts with different permission levels exist
- Manual testing tools or browser DevTools available

---

**Test Cases**

TC-SEC-01 – SQL injection prevention on login

Steps:
1. Enter SQL injection payload in login fields
2. Submit login request

Expected Result: System rejects input and does not expose database or internal errors.

---

TC-SEC-02 – Cross-site scripting (XSS) prevention

Steps:
1. Insert malicious script into a text input field
2. Submit the form

Expected Result: System escapes input and prevents script execution.

---

TC-SEC-03 – Password strength enforcement

Steps:
1. Attempt to register using a weak password
2. Submit the form

Expected Result: System rejects weak passwords and displays validation message.

---

TC-SEC-04 – Unauthorized access attempt

Steps:
1. Attempt to access restricted area without proper permissions

Expected Result: System blocks access and redirects user to login or displays authorization error.

---

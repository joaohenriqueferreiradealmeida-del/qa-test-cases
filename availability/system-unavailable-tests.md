**System Unavailability – Test Cases**

**Objective:**
Validate system behavior during service downtime, ensuring proper error handling, user-friendly messaging, and prevention of technical error exposure.

**Scope:**
These test cases cover scenarios where the system is unavailable, including full downtime and internal server errors (HTTP 500).

**Preconditions:**
- System may be partially or fully unavailable
- User attempts to access public pages (home, login, signup)

---

**Test Cases**

TC-FA-02 – Page unavailable without user message

Steps:
1. Access the home page
2. Reload the page

Expected Result:
- System displays a clear and user-friendly message informing that the service is temporarily unavailable

Actual Result: 
- Page remains blank
- No message is displayed to the user
Status: FAIL

---

**TC-FA-03 – Internal Server Error (500) handled correctly**

Steps:
1. Access the login page
2. Reload the page

Expected Result:
- Error 500 occurs without exposing technical details
- Friendly message displayed to the user

Actual Result:
- Error handled correctly
- Friendly message displayed
Status: PASS

---

TC-FA-04 – Internal Server Error exposes technical details

Steps:
1. Access the login page
2. Reload the page

Expected Result:
- Error 500 without exposing system or stack trace details
- Friendly message displayed to the user

Actual Result:
- Technical error details displayed
- No user-friendly message shown
Status: FAIL

---

**TC-FA-05 – User receives clear guidance during system downtime**

Steps:
1. Access the signup page
2. Attempt to fill required fields
3. Try to proceed to the next step

Expected Result:
- Clear and friendly message informing service unavailability
- Guidance on what the user should do next (retry later)
- Page layout remains visible

Actual Result:
- Friendly message displayed
- Layout preserved
- Proper user guidance provided
Status: PASS

---

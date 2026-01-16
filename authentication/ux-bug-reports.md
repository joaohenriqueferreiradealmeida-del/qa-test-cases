**UX – Authentication User Experience Bug Reports**

**Objective:**
Identify user experience issues related to authentication flows that may negatively impact usability, clarity, and user satisfaction.

**Scope:**
These bug reports include:
- Error message clarity
- Feedback provided to users
- Exposure of technical or system-level errors
- General usability issues in authentication flows

**Out of scope:**
- Visual design improvements
- Performance issues

**Test Environment:**
- Application Type: Web Application
- Module: Authentication – UX
- Browser: Google Chrome
- Operating System: Windows
- Environment: Test / Staging

**Preconditions:**
- System is online
- Authentication pages are accessible

**Test Type:**
- Manual Testing
- Usability Testing

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


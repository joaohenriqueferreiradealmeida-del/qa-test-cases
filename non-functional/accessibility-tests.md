**Test Cases – Accessibility (Non-Functional)**

**Objective:**
Ensure the application is accessible to users with disabilities, following WCAG accessibility guidelines.

**Scope:**
These test cases validate keyboard navigation, screen reader compatibility, text readability, and visual accessibility.

**Preconditions:**
- Application is accessible via browser
- Accessibility tools (e.g., Lighthouse, screen reader) available

---

**Test Cases**

TC-ACC-01 – Keyboard-only navigation

Steps:
1. Navigate through the application using only the keyboard
2. Attempt to submit forms using Enter key

Expected Result: All interactive elements are reachable and usable without a mouse.

---

TC-ACC-02 – Alternative text for images

Steps:
1. Inspect image elements on the page
2. Verify presence of descriptive alt text

Expected Result: All images contain meaningful alternative text.

--- 

TC-ACC-03 – Color contrast compliance

Steps:
1. Measure text contrast using accessibility tools

Expected Result: Text meets minimum contrast ratio for readability.

---

TC-ACC-04 – Screen reader compatibility

Steps:
1. Navigate the application using a screen reader
2. Observe reading order and clarity

Expected Result: Content is read logically and without confusion.

---

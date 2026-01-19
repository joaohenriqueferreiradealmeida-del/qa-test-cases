**Bug Reports – System Stability & Error Handling**

**Objective**
Identify failures related to system instability, error handling, security exposure, and lack of resilience during unexpected failures, ensuring proper user feedback and system reliability.

**Scope**
- Server errors handling (5xx)
- User-facing error messages
- System observability and logging
- Transaction integrity during system failures

**Out of Scope**
- Functional business rules
- UI layout improvements unrelated to system errors

**Test Environment**
- Application Type: Web Application
- Browser: Google Chrome
- Operating System: Windows
- Environment: Test / Staging

**Test Type**
- Manual Testing
- Exploratory Testing
- Negative Testing

--

**CT-BUG-01 — System displays raw HTTP 500 error without user-friendly message**

**Description:**
When an internal server error occurs, the system displays a raw HTTP 500 error to the end user instead of a friendly and informative message.

**Preconditions:**
- User is registered
- System is online

**Steps to Reproduce:**
1. Access the website
2. Navigate to any internal page
3. Reload the page during an internal error

**Expected Result:**
- A friendly error message is displayed
- User is informed about the issue and guided to retry later

**Actual Result:**
- A blank page with HTTP 500 error is shown

**Severity:** Medium
**Priority:** Medium
**Status:** Open
**Evidence:** Screenshot showing HTTP 500 error page

---

**CT-BUG-02 — Technical backend error exposed to end user**

**Description:**
Internal system exceptions are exposed directly to the user, revealing backend implementation details and posing a security risk.

**Preconditions:**
- System online
- User authenticated

**Steps to Reproduce:**
1. Access the “My Orders” page
2. Simulate database connection failure

**Expected Result:**
- A generic, user-friendly error message is displayed
- No technical details are exposed

**Actual Result:**
Raw backend exception displayed:
PDOException: SQLSTATE[HY000]...

**Severity:** High
**Priority:** High
**Status:** Open
**Evidence:** Screenshot showing exposed backend error

---

**CT-BUG-03 — System does not log critical service unavailability**

**Description:**
Critical system failures are not registered in monitoring or logging tools, preventing the technical team from detecting incidents.

**Preconditions:**
- Access to system logs dashboard
- System online

**Steps to Reproduce:**
1. Force authentication service downtime
2. Attempt to log in
3. Check system logs

**Expected Result:**
- Error logged with correct timestamp
- Message indicating authentication service failure

**Actual Result:**
- No logs registered despite service outage

**Severity:** Critical
**Priority:** High
**Status:** Open
**Evidence:** Comparison between user error screen and empty logs dashboard

---

**CT-BUG-014 — System allows critical action while database is offline**

**Description:**
The system allows users to complete critical actions even when backend services are unavailable, causing data inconsistency.

**Preconditions:**
- User logged in
- Database service offline

**Steps to Reproduce:**
1. Add products to cart
2. Proceed to checkout
3. Finalize purchase while database is offline

**Expected Result:**
- System blocks the action
- User is notified that the operation cannot be completed

**Actual Result:**
- Success message displayed
- Order is not saved in the system

**Severity:** Critical
**Priority:** High
**Status:** Open
**Evidence:** Video showing success message followed by missing order

---

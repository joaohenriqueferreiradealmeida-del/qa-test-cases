**Test Cases – Performance (Non-Functional)**

**Objective:**
Validate system performance under normal and stress conditions, ensuring acceptable response times, stability under load, and smooth user experience.

**Scope:**
These test cases cover page load performance, response time under concurrent usage, and system behavior during stress scenarios.

**Preconditions:**
- Application is deployed and accessible
- Test environment is stable
- Browser DevTools or basic load testing tools are available

---

**Test Cases**

**TC-PERF-01 – Initial page load time**

Steps:
1. Open the application homepage
2. Measure full page load time using browser DevTools

Expected Result: Page loads completely in less than 3 seconds with no critical slow resources.

---

TC-PERF-02 – Search response under concurrent access

Steps:
1. Perform multiple search requests simultaneously
2. Measure average response time

Expected Result: Search responses return within acceptable latency (<500ms) without system crashes.

---

TC-PERF-03 – Checkout performance with multiple items

Steps:
1. Add multiple items to the cart
2. Initiate checkout
3. Measure time until confirmation

Expected Result: Checkout completes successfully in less than 5 seconds.

---

TC-PERF-04 – System stability under stress

Steps:
1. Perform repeated invalid search requests
2. Monitor system behavior and response time

Expected Result: System remains stable, does not return server errors, and maintains acceptable response times.

---

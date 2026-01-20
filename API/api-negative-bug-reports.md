**API – Bug Reports & Negative Test Scenarios**

**BR-API-01 – API returns HTTP 200 for invalid request**

**Objective:**
Validate whether the API returns the appropriate HTTP status code when receiving an invalid request.

**Preconditions:**
- Endpoint is available and accessible
- API is running in a test or staging environment

**Test Steps:**
1. Send a request to the endpoint with an invalid or incomplete payload
2. Observe the HTTP status code returned

**Expected Result:**
- The API should return an HTTP 4xx status code (e.g., 400 Bad Request or 422 Unprocessable Entity)
- The response should contain a clear validation error message

**Actual Result:**
The API returns 200 OK even when the request is invalid

**Severity:** High

**Notes:**
Returning status 200 may mislead client applications into interpreting the request as successful.

---

**BR-API-02 – Required fields are not validated in request payload**

**Objective:**
Verify whether the API properly validates required fields in the request payload.

**Preconditions:**
- Endpoint is active
- API documentation defines mandatory fields

**Test Steps:**
1. Send a request omitting one or more required fields
2. Analyze the API response

**Expected Result:**
- The API should reject the request
- Return HTTP status 400 or 422
- Inform which required fields are missing

**Actual Result:**
The API processes the request even when required fields are missing

**Severity:** Critical

**Notes:**
Lack of validation compromises data integrity and may lead to inconsistent system behavior.

---

**BR-API-03 – API accepts invalid data types**

**Objective:**
Validate whether the API rejects payloads containing data types that do not match the defined contract.

**Preconditions:**
- API contract is documented
- Endpoint is accessible

**Test Steps:**
1. Send a request using incorrect data types (e.g., string instead of number)
2. Verify the API response

**Expected Result:**
- Request should be rejected
- HTTP status 422 returned
- Error message indicating invalid data type

**Actual Result:**
- The API accepts the invalid payload and processes the request

**Severity:** High

**Notes:**
This behavior may cause failures in integrations and unexpected errors in consuming systems.

---

**BR-API-04 – Sensitive data exposed in API response**

**Objective:**
Ensure that the API does not expose sensitive data in its responses.

**Preconditions:**
- Authenticated endpoint
- Sensitive data exists in the system

**Test Steps:**
1. Perform a valid request to the endpoint
2. Analyze the response body

**Expected Result:**
- Response should contain only allowed fields
- No sensitive information (e.g., passwords, tokens, internal IDs) should be exposed

**Actual Result:**
- Sensitive data is returned in the API response

**Severity:** Critical

**Notes:**
This issue represents a serious security risk and may violate data protection and privacy regulations.

---

**BR-API-05 – Incorrect HTTP status returned for authentication failure**

**Objective:**
Validate whether the API returns the correct HTTP status code when authentication fails.

**Preconditions:**
- Endpoint protected by authentication

**Test Steps:**
1. Send a request using an invalid or expired token
2. Verify the response status code

**Expected Result:**
- API should return HTTP 401 Unauthorized
- Clear authentication error message

**Actual Result:**
- API returns an incorrect status code (e.g., 200 or 403 without proper context)

**Severity:** High

**Notes:**
Incorrect status codes make error handling difficult for client applications.

---

**BR-API-06 – Protected endpoint allows access without authentication token**

**Objective:**
Ensure that protected endpoints enforce authentication requirements.

**Preconditions:**
- Endpoint configured to require authentication

**Test Steps:**
1. Send a request to the endpoint without an authentication token
2. Analyze the response

**Expected Result:**
- Request should be blocked
- HTTP 401 Unauthorized returned

**Actual Result:**
- API allows access without authentication

**Severity:** Critical

**Notes:**
This is a severe security flaw that may allow unauthorized access to sensitive data and operations.

---

**BR-API-07 – API response breaks contract definition**

**Objective:**
Validate whether the API response strictly follows the documented contract.

**Preconditions:**
- API contract documented
- Endpoint is active

**Test Steps:**
1. Send a valid request
2. Compare the response structure with the documented contract

**Expected Result:**
- Response must fully match the contract (fields, data types, structure)

**Actual Result:**
- Missing fields, extra fields, or mismatched data types are returned

**Severity:** High

**Notes:**
Breaking the API contract may cause failures in client applications and system integrations.

---

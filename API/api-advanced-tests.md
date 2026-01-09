**Test Cases – API (Advanced)**

**Objective:**
Validate advanced API behaviors to ensure correct handling of authentication, authorization, data validation, HTTP methods, and error responses according to RESTful standards.

**Scope:**
These test cases cover positive and negative scenarios for REST APIs, including authentication, CRUD operations, validation rules, and security-related responses.

**Preconditions:**
- API environment is available and running
- API base URL is accessible
- Valid authentication token exists (when applicable)
- Requests executed using tools like Postman or Insomnia

---

**Test Cases**

TC-API-ADV-01 – Retrieve user data with valid authentication token

Steps:
1. Send a GET request to /users/{id}
2. Include a valid Authorization Bearer token in headers

Expected Result: API returns status code 200 and a JSON response containing the user data.

---

TC-API-ADV-02 – Create new resource with valid request body

Steps:
1. Send a POST request to /items
2. Provide a valid JSON body with required fields

Expected Result: API returns status code 201 and the newly created resource ID.

---

TC-API-ADV-03 – Update existing resource with invalid request body

Steps:
1. Send a PUT request to /items/{id}
2. Provide an invalid or incomplete JSON body

Expected Result: API returns status code 400 with an error message indicating invalid input data.

---

TC-API-ADV-04 – Delete resource without authentication token

Steps:
1. Send a DELETE request to /items/{id}
2. Do not include Authorization token in headers

Expected Result: API returns status code 401 indicating unauthorized access.

---

TC-API-ADV-05 – Access protected endpoint with invalid token

Steps:
1. Send a GET request to /user/profile
2. Include an invalid or expired Authorization token

Expected Result: API returns status code 401 with an authentication error message.

---

TC-API-ADV-06 – Handle rate limiting after multiple requests

Steps:
1. Send multiple consecutive requests to the same endpoint within a short time
2. Exceed the allowed request limit

Expected Result: API returns status code 429 indicating too many requests.

---

TC-API-ADV-07 – Validate response structure and mandatory fields

Steps:
1. Send a valid GET request to a user endpoint
2. Inspect the response body structure

Expected Result: Response contains all mandatory fields and follows the expected JSON schema.

---

TC-API-ADV-08 – Reject unsupported HTTP method

Steps:
1. Send an unsupported HTTP method (e.g., PATCH) to a restricted endpoint

Expected Result: API returns status code 405 indicating method not allowed.

---

**Notes**
- Status codes validated according to REST standards
- Focus on security, data integrity, and API reliability
- Suitable for both manual API testing and automated test design

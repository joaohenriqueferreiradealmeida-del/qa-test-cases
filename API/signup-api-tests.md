**API Test Cases – User Registration (Sign Up)**

**Objective**
Validate the user registration API to ensure that new users can be created successfully with valid data and that the system properly handles validation rules, HTTP methods, and error scenarios.

**Scope**
These test cases cover positive and negative scenarios related to the user registration API endpoint.

**Preconditions**
- API is available and accessible
- Endpoint /cadastro is active
- Test environment is properly configured

---

**Test Cases**

**TC-API-01 – Create user with valid data**

Method: POST
Endpoint: /cadastro

Steps:
1. Send a POST request with valid user data
2. Observe the API response

Test Data:
- Username: usuario_teste
- Email: usuarioteste@email.com
- Password: senha@123
- Confirm Password: senha@123

Expected Result:
- API returns HTTP status 201 Created
- Success message confirming user creation
- No authentication token returned
Result: PASS

---

**TC-API-02 – Create user with already registered email**

Method: POST
Endpoint: /users

Steps:
1. Send a POST request using an email that already exists
2. Observe the API response

Test Data:
- Name: João Teste
- Email: joao@email.com
- Password: Senha@123

Expected Result:
- API returns HTTP status 409 Conflict
- Error message indicating email already registered
Result: PASS

---

**TC-API-03 – Create user with password shorter than minimum length**

Method: POST
Endpoint: /cadastro

Steps:
1. Send a POST request with a password shorter than 6 characters
2. Observe the API response

Test Data:
- Password: 12345

Expected Result:
- API returns HTTP status 400 Bad Request
- Error message informing minimum password length requirement
Result: PASS

---

**TC-API-04 – Create user with missing required field (email)**

Method: POST
Endpoint: /cadastro

Steps:
1. Send a POST request without the email field
2. Observe the API response

Expected Result:
1. API returns HTTP status 400 Bad Request
2. Validation error indicating the email field is required
Result: PASS

---

**TC-API-05 – Attempt to create user using invalid HTTP method**

Method: GET
Endpoint: /cadastro

Steps:
1. Send a GET request to the registration endpoint
2. Observe the API response

Expected Result:
- API returns HTTP status 405 Method Not Allowed
- Error message instructing to use POST method
Result: PASS

---

Notes
- Test cases focus on validation rules, business logic, and correct HTTP method usage
- Duplicate or inconsistent cases were removed to maintain clarity and quality

---

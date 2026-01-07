Test Cases – Login (Security & Business Rules)

Objective:
Validate the login functionality with emphasis on security rules, account lockout behavior, and correct system responses after failed authentication attempts.

Scope:
These test cases cover positive flows, negative scenarios, and security-related behaviors for the user login feature.

Preconditions:
- User is on the login page
- System is online and accessible
- User account exists in the system (unless stated otherwise)

---

Test Cases

TC-LOGIN-01 – Login with valid credentials

Steps:
1. Enter a valid registered email
2. Enter the correct password
3. Click the "Login" button

Expected Result:
User is successfully authenticated and redirected to the dashboard.

---

TC-LOGIN-02 – Login with invalid password

Steps:
1. Enter a valid registered email
2. Enter an incorrect password
3. Click the "Login" button

Expected Result:
System displays an authentication error message indicating invalid credentials.

--- 

TC-LOGIN-03 – Account lockout after three consecutive failed attempts

Steps:
1. Enter a valid email
2. Enter an incorrect password
3. Repeat the process three consecutive times

Expected Result:
User account is temporarily blocked after the third failed attempt, and a lockout message is displayed.

---

TC-LOGIN-04 – Login attempt during account lockout period

Steps:
1. Enter a valid email for a blocked account
2. Enter the correct password
3. Click the "Login" button

Expected Result:
System prevents login and displays a message informing the user that the account is temporarily blocked.

---

TC-LOGIN-05 – Login before lockout time expires

Steps:
1. Trigger account lockout
2. Attempt login before the lockout duration has elapsed

Expected Result:
System does not allow login and maintains the account in blocked status.

---

TC-LOGIN-06 – Login after lockout period expires

Steps:
1. Trigger account lockout
2. Wait until the lockout time expires
3. Enter valid credentials
4. Click the "Login" button

Expected Result:
User is successfully authenticated, and the account lockout is lifted.

---

TC-LOGIN-07 – Reset of failed attempt counter after successful login

Steps:
1. Enter incorrect password twice
2. Enter correct credentials on the third attempt
3. Logout
4. Attempt login again with an incorrect password

Expected Result:
Failed attempt counter is reset after successful login, and account is not blocked prematurely.

---

TC-LOGIN-08 – Account remains blocked if browser is closed

Steps:
1. Trigger account lockout
2. Close the browser
3. Reopen the browser
4. Attempt login with valid credentials

Expected Result:
Account remains blocked until the lockout period expires.

---

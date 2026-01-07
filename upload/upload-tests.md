# File Upload – Test Cases

## Objective
Validate the file upload functionality, ensuring that only supported file types and sizes are accepted, and that the system properly handles error scenarios and interruptions.

## Scope
These test cases cover functional, validation, and negative scenarios related to file upload.

## Preconditions
- User is authenticated
- System is online and accessible
- File upload feature is enabled

---

## Test Cases

### TC-UPLOAD-01 – Upload file with valid format and size
**Steps:**
1. Access the system
2. Select a JPG file with size up to 5MB
3. Choose the destination folder
4. Click the "Upload File" button

**Expected Result:**
- File is uploaded successfully
- System displays upload success confirmation

---

### TC-UPLOAD-02 – Upload file with unsupported format
**Steps:**
1. Access the system
2. Select a file with unsupported format (PDF or EXE)
3. Click the "Upload File" button

**Expected Result:**
- Upload is blocked
- System displays an error message indicating invalid file format

---

### TC-UPLOAD-03 – Upload file exceeding size limit
**Steps:**
1. Access the system
2. Select a JPG file larger than 5MB
3. Click the "Upload File" button

**Expected Result:**
- Upload is blocked
- System displays an error message indicating file size exceeds the allowed limit

---

### TC-UPLOAD-04 – Upload interrupted during process
**Steps:**
1. Access the system
2. Start uploading a valid JPG file
3. Interrupt the upload (network failure or manual interruption)

**Expected Result:**
- Upload is canceled
- System displays a message requesting the user to try again
- System remains stable without freezing or crashing

---

### TC-UPLOAD-05 – Upload file with special characters in filename
**Steps:**
1. Access the system
2. Select a valid JPG file with special characters in the filename
3. Click the "Upload File" button

**Expected Result:**
- System handles the filename safely (error message or automatic renaming)
- File is not corrupted
- No unexpected characters are displayed

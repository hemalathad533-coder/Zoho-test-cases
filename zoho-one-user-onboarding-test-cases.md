 Zoho One: User Onboarding Test Cases


Module: Zoho One Directory (user management)

Scope: Add user, email verification, OTP verification, application access, role permissions, first login, deactivation

Tested by:Hemalatha D

Flow under test:

Open Zoho One → 

Directory → Add user →

fill profile (name, email, phone are mandatory) → 

user receives verification email → 

clicks link → OTP verification → 

completes account details → account confirmed →

admin assigns applications and permissions (Standard, Admin, Manager, etc.) → user logs in with email and password.

| ID | Scenario | Steps | Expected Result | Actual Result | Status |
|----|----------|-------|-----------------|---------------|--------|
| TC01 | Open Directory from Zoho One | Log in to Zoho One, open the apps list, select Directory | Directory opens with the Add user and Deactivate options | Directory opened with Add user and Deactivate options | Pass |
| TC02 | Add user with all mandatory fields | Click Add user, enter name, email and phone, save | User is added and a verification email is sent | User added and verification email sent | Pass |
| TC03 | Add user with empty name | Leave name empty, fill email and phone, save | Error message is shown, user is not created | Not tested | |
| TC04 | Add user with empty email | Leave email empty, fill name and phone, save | Error message is shown, user is not created | Not tested | |
| TC05 | Add user with empty phone number | Leave phone empty, fill name and email, save | Error message is shown, user is not created | Not tested | |
| TC06 | Add user with invalid email format | Enter an email without @, save | Validation error is shown | Not tested | |
| TC07 | Add user with invalid phone number | Enter letters in the phone field, save | Validation error is shown | Not tested | |
| TC08 | Add user with an email that already exists | Use the email of an existing user, save | System blocks it and shows an already-exists message | Not tested | |
| TC09 | Verification email is received | After adding the user, check the user's inbox | Verification email from Zoho arrives with a link | Verification email received with a link | Pass |
| TC10 | Verification link works | Click the link in the verification email | Link opens and asks for OTP verification | Link opened and asked for OTP verification | Pass |
| TC11 | OTP verification with the correct OTP | Enter the correct OTP | OTP is accepted and the user moves to the next step | OTP accepted and moved to the next step | Pass |
| TC12 | OTP verification with a wrong OTP | Enter an incorrect OTP | Error message is shown and access is not given | Not tested | |
| TC13 | Complete account details after OTP | Fill in the details Zoho asks for and submit | Account is confirmed | Account details completed and account confirmed | Pass |
| TC14 | Application access after confirmation | After the account is confirmed, check the user's access | User gets access to the assigned applications | User received application access | Pass |
| TC15 | Assign applications to a user | In Directory, select the user and choose the required applications | Selected applications appear for the user | Applications assigned based on the user's need | Pass |
| TC16 | Assign Standard permission | Set the user's permission to Standard for an application | User gets standard-level access only | Not tested | |
| TC17 | Assign Manager permission | Set the user's permission to Manager | User gets manager-level access | Not tested | |
| TC18 | Assign Admin permission | Set the user's permission to Admin | User gets admin-level access | Not tested | |
| TC19 | User sees only assigned applications | Log in as the user and view the applications | Only assigned applications are available | Not tested | |
| TC20 | First login with email and password | Log in as the new user with email and password | User logs in and can open the assigned applications | User logged in and accessed the assigned applications | Pass |
| TC21 | Login with a wrong password | Enter the correct email and a wrong password | Error message is shown and login is blocked | Not tested | |
| TC22 | Deactivate a user | In Directory, select the user and choose Deactivate | User is deactivated | Not tested | |
| TC23 | Deactivated user tries to log in | Log in using the deactivated user's credentials | Login is blocked | Not tested | |

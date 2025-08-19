## If a user logs in and it’s been more than 90 days since their password has been reset, they need to be redirected to the password change page.

### Steps
1. Attempt to login using valid credentials for a user that has not **reset their password** in over 90 days
2. Confirm that the user cannot proceed further if they have not successfully updated their password.
	1. Attempt to navigate to a URL directly or from a bookmark
3. Show a popup message saying “Your password has expired, because it’s been 90 days since the last reset. Please change your password to continue.” When I click “I understand” the pop up goes away

### Expected Result
1. The user Cannot proceed if their password has not been reset in over 90 days


## If a user logs in and it’s been less than 90 days since their password has been reset, they need to login normally

### Steps
1. Attempt to login using valid credentials for a user that has **reset their password** in the last 90 days
2. Confirm that you are directed to the pipeline view
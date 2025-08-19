test-230
Upon login, I should be redirected to my profile page so that I can enter my phone number

Show a message on the profile page "Your organization requires two-factor authentication (2FA), but no phone number is associated with your account. Please enter a valid phone number to complete the 2FA setup.”

The user can’t access another URL until they have entered their phone number and saved.


## Upon login, I should be redirected to my profile page so that I can enter my phone number
### Steps
1. Login with a user that has valid credentials and no number associated to their profile
2. Confirm that the user is redirected to update their details and is shown a message on the profile page "Your organization requires two-factor authentication (2FA), but no phone number is associated with your account. Please enter a valid phone number to complete the 2FA setup.”
3. Confirm that the user cannot manually enter a url to navigate away from the update details screen

### Expected Results
1. the user is redirected to update their details and is shown a message on the profile page "Your organization requires two-factor authentication (2FA), but no phone number is associated with your account. Please enter a valid phone number to complete the 2FA setup.”
2. the user cannot manually enter a url to navigate away from the update details screen

## Users with a number associated to their profiles should not be asked to update their details
### Steps
1. Login with a user that has valid credentials and a number associated to their profile

### Expected Result
1. The user should not be prompted to update their details
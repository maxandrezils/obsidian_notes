1. When a user logs in to MDX, the system will check if they are active.
2. If the user is active, they can log in successfully.
3. If the user is **not** active because they have not logged in for 90 days, their account should be flagged as `inactive`
4. The user should also see a message on the log in screen saying “Your account has been deactivated due to inactivity. Please contact your manager to have it reactivated.”

## If the user is active, they can log in successfully.
### Steps
1. Attempt to login with a valid user that has logged in the last 0 - 89 days
2. Confirm that the check for if the user is active occurs and the user is successfully logged in

### Expected Result
1. the check for if the user is active occurs and the user is successfully logged in


## If the user is **not** active because they have not logged in for 90 days, their account should be flagged as `inactive`
### Steps
1. Attempt to login with a valid user that has logged in the last 90 days
2. Confirm that the check occurs and flags the user as inactive

### Expected Results
1. The user should also see a message on the log in screen saying “Your account has been deactivated due to inactivity. Please contact your manager to have it reactivated.”
2. The user should be flagged as inactive in admin


## After a user has been deactivated and reactivated due to inactivity, they should be able to login
### Steps
1. Attempt to login with a valid user that has logged in the last 90 days
2. Confirm that the check occurs and flags the user as inactive
3. Re-activate the user as a client manager using the user management screen
4. Confirm that the user can now login

### Expected result
1. After being reactivated by the client manager, the user should be able to login
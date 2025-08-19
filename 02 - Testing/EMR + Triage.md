
## Update routing configuration for surgeries to set the eMR+ dashboard as the default landing page.
### Routing for the homepage should be updated to: eMR+ dashboard for eMR+ surgeries for all user types > Whitelisted IP
### Steps
1. As a user associated to an eMR+ surgery, that has requested to have their IP whitelisted login to the EMR portal

### expected result
The user is directed to the EMR+ dashboard as the default home page after logging in


## Update routing configuration for surgeries to set the eMR+ dashboard as the default landing page.
### Routing for the homepage should be updated to: eMR+ dashboard for eMR+ surgeries for all user types > Non - Whitelisted IP | 2FA Enabled
### Steps
1. As a user associated to an eMR+ surgery, that has 2FA enabled and has not been whitelisted
2. you are requested to enter an OTP and receive one to the number associated to the user
3. on successful 2FA< you are directed to the eMR+ dashboard

### expected result
The user is directed to the EMR+ dashboard as the default home page after logging in


## Ensure other practice staff roles default to the **Instruction Pipeline** view.
### Routing for homepage should remain the same if the surgery is not an eMR+ surgery > whitelisted ip

### Steps
1. as a non-emr+ user that has whitelisted their IP, login to the emr portal
2. confirm that you are directed to the instruction pipeline view

Expected Res
you are directed to the instruction pipeline view



## Ensure other practice staff roles default to the **Instruction Pipeline** view.
### Routing for homepage should remain the same if the surgery is not an eMR+ surgery > non-whitelisted ip

### Steps
1. as a non-emr+ that has 2FA enabled and has not been whitelisted
2. you are requested to enter an OTP and receive one to the number associated to the user
3. on successful 2FA< you are directed to the instruction pipeline view

Expected Res
you are directed to the instruction pipeline view


## Clam AV

# ClamAV Setup
## Confirm that documents are being scanned
### steps
1. before a pre-instruction is created, clam av should scan the attachments and check for viruses


# ClamAV Validation: threat
## Confirm that if there is a threat, the instruction is not created
### Steps.
1. Upload a document with a threat associated to it
2. Confirm that ClamAV picks up the threat and "rejects" the instruction

ClamAv detects the threat and prevents the instruction from being created
 
# Create post endpoint in eMR
## Confirm that there is an api endpoint that can receive and update the classification of pre-instructions
### Steps
1. Create a pre-instruction 
2. confirm that classification is updated at the end of the triaging process

The classification for the report is updated

# Endpoint updates the status and confidence correctly.
## Confirm that based on the triaging workflow, the correct post request is sent

### Steps
1. Based on the scenarios in https://medi2data.atlassian.net/browse/TEST-316, confirm that each scenario results in the correct response from the endpoint

The correct responses are sent
# Add authentication using api key

## Confirm that you cannot update a pre-instruction from postman without an authentication key
### Steps
1. Request the endpoint be added to the postman collection or ask for the curl of the request 
2. Attempt to update a pre-instruction from Postman 

The request should fail on an auth error


# Handle invalid requests and failures elegantly
## Confirm that the endpoint will fail gracefully when invalid requests are sent
1. Request the endpoint be added to the postman collection or ask for the curl of the request 
2. Request the api key
3. send a request without a payload
4. send a request with an invalid payload

Confirm that the api will display an error and not update the pre-instruction
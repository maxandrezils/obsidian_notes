1. Add an optional parameter for **patient approval** in the `create instruction` endpoint.
    - Parameter: `patient_approval`
    - Values: `true` or `false`
    - Default: `false`
2. If `patient_approval` is `true`, require `patient email` and `patient phone number` parameters.
3. If `patient_approval` is not provided or is `false`, the `patient email` and `patient phone number` parameters are not required.
4. Add `country code` as a field that defaults to UK
5. Validation is required for the email + phone number
6. Update API documentation to reflect the new optional parameters and their usage.


## Add an optional parameter for **patient approval** in the `create instruction` endpoint.
## Steps
1. For the {{MDX EXTERNAL ENDPOINT}}/instructions/ endpoint, confirm that the request body can optionally include the following
	1. partient_approval: true | false
	2. has a default value of false if no parameter is included

## Including patient_approval: true as a parameter, requires you to include patient_email and patient_phone_number
### Steps
1. For the {{MDX EXTERNAL ENDPOINT}}/instructions/ endpoint, include patient_approval: true as a parameter in the response body without including the patient_email and patient_phone_number parameters.
2. Confirm that the response does not succeed and an appropriate message is displayed

### Expected Result
1. The request should not succeed, and an appropriate error message should be displayed


## Including patient_approval: true as a parameter, requires you to include patient_email and patient_phone_number > fields included
### Steps
1. For the {{MDX EXTERNAL ENDPOINT}}/instructions/ endpoint, include patient_approval: true as a parameter in the response body while including the patient_email and patient_phone_number parameters.
2. Confirm that the request succeeds and that the details are captured in the admin panel

### Expected Result
1. the instruction is created with the patient details included.


## Add `country code` as a field that defaults to UK
### Steps
1. For the {{MDX EXTERNAL ENDPOINT}}/instructions/ endpoint, include country_code as a parameter and leave it blank

### Expected Result
1. The instruction should be created with a default value of UK

## Patient_email and patient_phone_number has validation
### Steps
 1. For the {{MDX EXTERNAL ENDPOINT}}/instructions/ endpoint, include patient_email & patient_phone_number in incorrect formats

### Expected Result
1. Validation should prevent the instruction from being created with invalid details

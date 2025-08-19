- Medical reports can be retrieved from the MDX application following a successful GET request with valid parameters that would also successfully retrieve a medical report from the current eMR application.
    
- The medical report API has the same error-handling as the existing implementation of the API on eMR.
    
- The medical report API should have unit test coverage to ensure functionality.
    
- The medical report API is being used by existing clients and therefore it is imperative that the functionality and stability of the API is not affected.

## Medical reports can be retrieved from the MDX application following a successful GET request with valid parameters that would also successfully retrieve a medical report from the current eMR application. 
### Steps
1. In MDX Admin, mark an instruction as completed and upload a report
2. In Postman, with a valid api key associated to the above organisation, run the following request: ```{{MDX EXTERNAL ENDPOINT}}/pdf_report/<mdx_instruction_id> ``` using the above instruction's id and <Send & Download>
3. Confirm that the report downloaded is the one associated to the instruction.



### Expected Result
The correct report is sent and **downloaded**


## Medical reports can be retrieved  following a successful GET request with valid parameters that would also successfully retrieve a medical report from the current eMR application. 
### Steps
1. In EMR Admin, mark an instruction as completed and upload a report
2. In Postman, with a valid api key associated to the above organisation, run the following request: ```{{MDX EXTERNAL ENDPOINT}}/pdf_report/<mdx_instruction_id> ``` using the above instruction's EMR id and <Send & Download>
3. Confirm that the report downloaded is the one associated to the instruction.



### Expected Result
The correct report is sent and **downloaded**

## Medical reports cannot be retrieved  without a valid API Key
### Steps
1. In EMR Admin, mark an instruction as completed and upload a report
2. In Postman, remove the valid api key associated to the above organisation, run the following request: ```{{MDX EXTERNAL ENDPOINT}}/pdf_report/<mdx_instruction_id> ``` using the above instruction's EMR id and <Send & Download>
3. Confirm that you do not receive the medical report



### Expected Result
you receive a 403 error and the following json response:
```
{

    "detail": "Authentication credentials were not provided."

}
```
\

## Medical reports cannot be retrieved  without a valid instruction ID
### Steps
1. In EMR Admin, mark an instruction as completed and upload a report
2. In Postman, with an API Key associated to the above organisation, run the following request: ```{{MDX EXTERNAL ENDPOINT}}/pdf_report/<invalid_mdx_instruction_id> ``` using an invalid id and <Send & Download>
3. Confirm that you do not receive the medical report



### Expected Result
you receive a 400 error and the following json response:
```
{
    "message": "Invalid request - [CODE] [PG00034]",
    "error_code": "[PG00034]"
}
```

## Medical reports cannot be retrieved for rejected instructions
### Steps
1. In MDX Admin, reject a previously created instruction
2. In Postman, with a valid api key associated to the above organisation, run the following request: ```{{MDX EXTERNAL ENDPOINT}}/pdf_report/<mdx_instruction_id> ``` using the above instruction's id and <Send & Download>
3. Confirm that you do not receive the medical report and get the correct error

### Expected Result

The response shoud send an HTTP Status: 422, and the json should include the correct reason, note, error code and timestamp in the below format
```json
{
    **"message": "Rejected instruction",
    "reason": "Inappropriate consent / consent not properly obtained",
    "note": "inappropriate consent test 1",
    "rejected_timestamp": "2024-03-25 10:16:54",
    "error_code": "PG00048"**
}
```


## Medical reports cannot be retrieved for instructions that have not been completed
1. Create a new MDX instruction using the client interface and note the instruction ID
2. In Postman, with a valid api key associated to the above organisation, run the following request: ```{{MDX EXTERNAL ENDPOINT}}/pdf_report/<mdx_instruction_id> ``` using the above instruction's id and <Send & Download>
3. Confirm that you do not receive the medical report and the API returns the appropriate error

### Expected Result
The API should return the below error

|         |     |                                                                                                                                                                                                                                           |                          |
| ------- | --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------ |
| PG00034 |     | [PDF API]: The organisation {client_org} has tried to access an instruction that does not have an associated medical report. And also in the case that the instruction status is invalid (i.e. not Completed, Paid, Invoiced, Downloaded) | 422 and 400 respectfully |

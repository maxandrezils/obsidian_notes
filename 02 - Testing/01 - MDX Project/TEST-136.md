1. The system should run a scheduled job (cron) at 12 PM and 6 PM daily to handle failed submissions.
2. The MDX backend should retrieve all failed online instructions from the MDX database.
    1. A failed instruction is one that has `Is gp surgery live` flag set to True. And `Successfully created on eMR` flag is NOT True.
3. For each failed instruction in status of “New”, the MDX backend should re-trigger the create_instruction API call to the eMR API.
4. The system should handle the response from the eMR API, updating the MDX database to indicate whether the re-triggered submission was successful or failed.
5. If the submission is successful, the failed flag should be cleared. If it fails again, the flag should remain and be retried in the next scheduled job.
6. The system should log the result of each re-trigger attempt, indicating whether it was successful or failed, ensuring transparency and allowing for manual review if necessary.


## The system should run a scheduled job (cron) at 12 PM and 6 PM daily to handle failed submissions.
### Steps
1. Create an Instruction associated to a live GP on MDX that is not created on EMR (you may have to request the connection to be severed between the two systems)
2. Confirm that the Successfully created on emr: flag is  False
3. Wait for the cron to run and confirm that the instruction is created on eMR and the Successfully created on emr: flag is True
### Expected Result
the instruction is created on eMR and the Successfully created on emr: flag is True

## The MDX backend should retrieve all failed online instructions from the MDX database. 
### Steps
1. Create an Instruction associated to an offline GP an MDX
2. Confirm that the Successfully created on emr: flag is  False
3. Wait for the cron to run and confirm that the flag is not updated and the instruction is not created in EMR
### Expected Result
the flag is not updated and the instruction is not created in EMR

## For each failed instruction in status of “New”, the MDX backend should re-trigger the create_instruction API call to the eMR API. 
> Note: The system should handle the response from the eMR API, updating the MDX database to indicate whether the re-triggered submission was successful or failed. If the submission is successful, the failed flag should be cleared. If it fails again, the flag should remain and be retried in the next scheduled job. The system should log the result of each re-trigger attempt, indicating whether it was successful or failed, ensuring transparency and allowing for manual review if necessary. are covered by this scenario
### Steps
1. <Instruction1>Create an Instruction associated to a live GP on MDX that is not created on EMR (you may have to request the connection to be severed between the two systems) 
2. <Instruction2>Create an Instruction associated to an offline GP an MDX
3. <Instruction3>Create an Instruction associated to a live GP on MDX that is not created on EMR (you may have to request the connection to be severed between the two systems) and update its status to in progress
### Expected Result
Confirm that only <Instruction1> is created in EMR






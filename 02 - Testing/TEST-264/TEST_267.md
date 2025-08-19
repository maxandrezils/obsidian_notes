## Create a new item in Administration, underneath Log entries, called `Expired Data Deletion Logs` to record the details of data that has been removed as part of the data retention process.
**Log Details:**
    - The log should capture the following details for each deleted item:
        - **MediRef**
        - **Surgery Name**
        - **Date of Removal**
#### Steps:
1. Run the data retention cron that removes instructions older than 6 years,
2. Confirm that the logs note the deleted instructions in the appropriate section

1. **Delete Expired Data:**
    1. Create a script to perform a hard deletion of medical reports that have reached their six-year retention limit, including any related patient information.
        
2. **Delete Soft-Deleted Instructions:**
    
    - Ensure the deletion process includes any instructions that were previously soft deleted but are now older than six years.
        
3. Delete the following for 1 and 2
    
    1. Instruction
        
    2. Medical report
        
    3. Any attachments associated with instruction
        
4. Verify that cascade delete is working so that patient data is also deleted when we delete the report.
    
5. **Timing:**
    
    1. The deletion must occur 30 days after the notification email is sent to the surgeries.
        
    2. So if the report is expiring in February
        
    3. The email needs to go out 1 Jan
        
    4. And the deletion happens 1 Feb
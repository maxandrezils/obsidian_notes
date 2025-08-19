# Triaging results are added as a deal note in HubSpot, and deal fields are updated accordingly.
##  Confirm that once triaging is completed, the deal notes are added to hubspot | success
### Steps:
1. Create a pre-instruction with a high chance of success 
2. wait for the triaging process to complete and confirm that it was successfully classified
3. In hubspot, confirm that the deal note has the expected note format

**Deal Note**
**Automated Triaging**

Predicted Report Type: {UC | PIP}
- - - **Full Name:** Mr. Steven Rutter (Confidence: 98.1%)
            
            **Date of Birth:** 18th January 1978 (Confidence: 99.2%)
            
            **Client Address:**
            
            Freepost RUGX-RKRT-GYGK
            
            Manchester BSC UC
            
            Mail Handling Site A
            
            Wolverhampton, WV98 2HQ
            
            (Confidence: 94.0%)
            
            **Patient Address:**
            
            27, The Quadrant, Droylsden, Manchester (Confidence: 70%)
            
            **Date Requested:** 2nd September 2024 (Confidence: 98.4%)
            
            **Note:** Confidence percentages indicate the accuracy of the extracted information.

# Pre-instruction values are compared with triaging results to validate accuracy.
# Confirm that the deal notes match the details in the uploaded attachments
### Steps
1. Create a pre-instruction with a high chance of success 
2. wait for the triaging process to complete and confirm that it was successfully classified
3. In hubspot, confirm that the deal note has the expected note 
4. Compare the details in the note to the details in the attachments

the details in the note should have a 95% accuracy
    
# The deal pipeline stage is updated to ‘Triaged’ when values match successfully.
# Confirm that when there is at least a 95% confidence, that the deal stage is updated to triaged.
### Steps
1. Create a pre-instruction with a high chance of success 
2. wait for the triaging process to complete and confirm that it was successfully classified
3. In hubspot, confirm that the deal stage has been updated to triaged.

The deal stage has been updated to triaged

    
# Discrepancies or low accuracy cases are logged with detailed field information for review.
## Confirm that low accuracy cases or discrepancies are logged in the deal notes

### Steps
1. Create a pre-instruction with a low chance of success 
2. wait for the triaging process to complete and confirm that it was successfully classified
3. In hubspot, confirm that the deal note has detailed information for review
The deal note is updated
    
# HubSpot deal updates reflect successful triaging, and all errors are logged for tracking.
## Confirm that errors are logged for tracking 

### Steps
1. if any errors are encountered during testing, they are logged

# Retries are accounted for in the hubspot integration
Refer to test details for https://medi2data.atlassian.net/browse/MEDI-4932
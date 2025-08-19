# The cloud function should use classifier output to identify what report type is being requested > UC
### Confirm that the classifier can correctly identify a UC report | >= 95%
### Steps
1. Create a pre-instruction using attachments that identify the pre-instruction as of type UC
2. Once the classification has completed and the post request from GCP has been sent to eMR, if the classification completed with over 95% confidence, the report should be classified correctly

The report is correctly classified as UC

# The cloud function should use classifier output to identify what report type is being requested > PIP
## Confirm that the classifier can correctly identify a PIP report | < 95%
### Steps
1. Create a pre-instruction using attachments that identify the pre-instruction as of type PIP
2. Once the classification has completed and the post request from GCP has been sent to eMR, if the classification completed with less than 95% confidence, the report should be Put on eMR+ commencement pipeline in NFS stage
3. Continue the process as normal

The report is correctly classified as PIP

# The cloud function should use classifier output to identify when an invalid report type is requested
## Confirm that the classifier can correctly identify an invalid report | >= 95%
### Steps
4. Create a pre-instruction using attachments that identify the pre-instruction as of type other
5. Once the classification has completed and the post request from GCP has been sent to eMR, if the classification completed with over 95% confidence, the report should be identified as of the wrong type

# The cloud function does not hallucinate classifications
## Confirm that the classifier can consistently identify a report
### Steps
1. Create a pre-instruction using attachments that identify the pre-instruction as of type UC that was used before and was correctly identified
2. repeat step 1 10 - 15 times and confirm that it always identifies the pre-instruction the same way
3. Create a pre-instruction using attachments that identify the pre-instruction as of type PIP  that was used before and was correctly identified
4. repeat step 2 10 - 15 times and confirm that it always identifies the pre-instruction the same way
5. Create a pre-instruction using attachments that identify the pre-instruction as of type other and was correctly identified that way
6. repeat step 5 10 - 15 times and confirm that it always identifies the pre-instruction the same way

# Error handling is implemented to manage classification failures, including retries for recoverable errors
## Confirm that failures in the process are handled gracefully
### Steps
1. In the event of an error, it is logged

# Logs are generated for all classification attempts, capturing success or failure details for debugging and monitoring. 
## Confirm that logs are generated for successful, low accuracy and non classifications and failures

### Steps
1. review that there are logs after completing all the previous scenarios
2. add a new pre-instruction and confirm that a new log is generated and timestamped

# **Low confidence classifications are Put on eMR+ commencement pipeline in NFS stage**
## **Confirm that reports with a confidence of > 95% are Put on eMR+ commencement pipeline in NFS stage**

### **Steps**
1. **Create a pre-instruction that you feel will be classified with a less than 95% accuracy**
2. **confirm that the pre-instruction is Put on eMR+ commencement pipeline in NFS stage**
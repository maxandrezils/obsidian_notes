| Issue key | Summary                                                                |
| --------- | ---------------------------------------------------------------------- |
| MEDI-4914 | [ECR0289]Add a cron to check TPP surgery status                        |
| MEDI-4882 | [ECR0358] TPP connection pop-up message wording :LiCircleCheckBig:     |
| MEDI-4881 | [ECR0363] Show Instruction ID on Third Party Authorisations Page       |
| MEDI-4854 | [ECR0289] Improve logs for TPP connection status dashboard             |
| MEDI-4711 | [BCR0139] ValueError: invalid literal for int() with base 10: 'SNOMED' |
| MEDI-4705 | [ECR0159] Edit sharing details for patient approval                    |
| MEDI-4704 | [ECR0036] Suggested items to add to be added in chronological order    |
| MEDI-4676 | Report Deletion Logs                                                   |
| MEDI-4675 | User Permissions Logic for Report Deletion                             |
| MEDI-4674 | Delete Buttons and Logic                                               |
## MEDI-4881
https://medi2data.atlassian.net/browse/TEST-253


## [MEDI-4704](https://medi2data.atlassian.net/browse/MEDI-4704)
1. When a user adds a new consultation, it should appear in chronological order within the list.
2. The list of consultations should always be sorted by date, including newly added items.
3. Ensure the sorting functionality is applied every time a new consultation is added.
4. Validate that the chronological order is maintained when viewing the consultations in any report.

### SAR Report -> Consultations are in chronological order  

#### Steps
1. Create a SAR report with a valid patient
2. Proceed to the provisional report page and confirm that the Consultations are in chronological order
3. proceed to the preview of the report and confirm that the report maintains the correct order for consultations
4. Finalise the report and confirm that the report maintains the correct order for consultations 

#### Expected Result
1. the report and confirm that the report maintains the correct order for consultations

### Insurance Report -> Consultations are in chronological order  

#### Steps
1. Create a Insurance report with a valid patient
2. Proceed to the provisional report page and confirm that the Consultations are in chronological order
3. proceed to the preview of the report and confirm that the report maintains the correct order for consultations
4. Finalise the report and confirm that the report maintains the correct order for consultations

#### Expected Result
1. the report and confirm that the report maintains the correct order for consultations


### DWP Report -> Consultations are in chronological order  

#### Steps
1. Create a DWP report with a valid patient
2. Proceed to the provisional report page and confirm that the Consultations are in chronological order
3. proceed to the preview of the report and confirm that the report maintains the correct order for consultations
4. Finalise the report and confirm that the report maintains the correct order for consultations

#### Expected Result
1. the report and confirm that the report maintains the correct order for consultations
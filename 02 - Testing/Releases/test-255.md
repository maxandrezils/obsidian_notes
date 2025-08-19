# Test-255
## Acceptance Criteria
1. Given the report is in the awaiting approval status, when I click on it and see the preview report, I can now see a button called ‘Edit Sharing Options’.
2. When I click on ‘Edit Sharing Options’, I see a modal called Patient approval details.
   1. Heading: Patient Approval Details
   2. Body: A report preview will be sent to the patient for review. If there is no response within 21 days, the report status will change to 'Completed.'
   3. Button `Cancel`: Go back to preview page
   4. Button `Update details`: Are you sure? Modal pops up
      1. Cancel: Go back to patient approval modal
      2. Confirm: Update the details and go back to preview report page.
3. Once the Update Details + Confirm buttons have been clicked, the patient approval **timer** should reset back to 0 and have a 21 day wait before auto approval.
4. Please prepopulate the email + phone number field if values already exist.

## Given the report is in the awaiting approval status, when I click on it and see the preview report, I can now see a button called ‘Edit Sharing Options’.
### Steps
1. For the different report types confirm that when you proceed to the awaiting approval status you can now see a button called ‘Edit Sharing Options’.
	1. SAR
	2. Insurance
	3. POA
	4. DWP
	5. MOD
	6. Other

### Expected Result
1. report is in the awaiting approval status, when I click on it and see the preview report, I can now see a button called ‘Edit Sharing Options’.

## When I click on ‘Edit Sharing Options’, I see a modal called Patient approval details.
### Steps
1. For the different report types confirm that when you proceed to the awaiting approval status you can now see a button called ‘Edit Sharing Options’.
2. When I click on ‘Edit Sharing Options’, I see a modal called Patient approval details.
3. Confirm that the patient details have been updated on the 

### Expected Result
Heading: Patient Approval Details
   2. Body: A report preview will be sent to the patient for review. If there is no response within 21 days, the report status will change to 'Completed.'
   3. Button `Cancel`: Go back to preview page
   4. Button `Update details`: Are you sure? Modal pops up
      1. Cancel: Go back to patient approval modal
      2. Confirm: Update the details and go back to preview report page.
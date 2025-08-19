# Hubspot deal created with valid fields
## Confirm that the deal is created correctly

### Steps
1. create a pre-instruction
2. In backoffice >> pre-instruction model, confirm that the deal has a hubspot deal id associated to it
3. In hubspot, using the deal id, confirm that all the fields are populated correctly

Expected Result
1. the deal id is associated to the instruction in back office
2. the deal was created successfully in hubspot 


# Combined PDF files are successfully uploaded for triaging.
## Confirm that the uploaded files are combined into a single pdf for triaging

### Steps
1. create a pre-instruction with multiple attachments
2.  In backoffice >> pre-instruction model, confirm that the deal has a hubspot deal id associated to it
3. In back office, confirm that the combined pdf is associated to the pre-instructon
4. In hubspot, using the deal id, confirm that the pdf has been associated correctly to the deal 

# Uploaded files are automatically converted to PDF format if not already in PDF.
## Confirm that the legal non-pdf files are converted to pdf 

### Steps
1. create a pre-instruction with multiple attachments that are not pdfs
2.   In backoffice >> pre-instruction model, confirm that the deal has a hubspot deal id associated to it
3. In back office, confirm that the combined pdf is associated to the pre-instruction
4. In hubspot, using the deal id, confirm that the pdf has been associated correctly to the deal 



# Multiple file objects are fetched from S3 and combined into a single PDF document.
## Confirm that the correct files are combined into a single pdf
### Steps
1. create a pre-instruction with multiple attachments 
2.  In backoffice >> pre-instruction model, confirm that the deal has a hubspot deal id associated to it
3. In back office, confirm that the combined pdf is associated to the pre-instruction and that the uploaded files are the ones that have been combined
4. In hubspot, using the deal id, confirm that the pdf has been associated correctly to the deal and that the uploaded files are the ones that have been combined

The correct files have been combined 


# Hubspot has instruction letter and consent added as combined files
## Confirm that hubspot has received the combined consent and instruction letter
### Steps
1. create a pre-instruction with multiple attachments 
2.  In backoffice >> pre-instruction model, confirm that the deal has a hubspot deal id associated to it
3. In hubspot, confirm that the deal has the combined consent and instruction letter associated to it 

hubspot,  deal has the combined consent and instruction letter associated to it 
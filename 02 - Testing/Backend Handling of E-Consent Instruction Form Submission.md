**Description (System Behaviour):**  
When the e-consent instruction form is submitted, the backend should persist the patient’s details to the relevant fields in the `Instruction` model, mark the instruction appropriately, and trigger downstream actions such as notifying the patient (in future)

#### A. Create & Populate Instruction

- On form submission, update the corresponding `Instruction` object
    
- 
- If **“No”** is selected for “Is the Claimant able to provide the required information and consent?”:
    
    - Still populate patient details but additional fill in alternative contact
        
    - populate `alternative_contact_relation`, `alternative_first_name`, `alternative_last_name`, and `alternative_email`
        
        - These fields will needed to be added to the `Instruction`model
            
- Always associate the instruction with:
    
    - `is_econsent_instruction = True`
        
    - `status = Awaiting Consent`
        

#### B. Notification Trigger

- This will be added in a later ticket
    

#### C. Contact details function

- Add model function to decide which contact details should be used (if alternative, use alternative)
    
- Update contact references in the code base to use function
    

### Validation & Security

- Ensure all submitted data is validated server-side (as per frontend requirements)
    
- Sanitize inputs before saving (e.g. stripping leading/trailing whitespace)
    
- Raise clear errors if required fields are missing or malformed
    
    - For FE errors, use same error messages as new instruction form
        
    - For BE errors, use logging standard
        
- Log form submission attempt with audit trail
    

### Acceptance Criteria:

-
    
- `is_econsent_instruction`, and `status` are not changed
    
- Instruction record is persisted and retrievable via admin and instruction pipeline views
    
- All form data is validated on submission with meaningful error responses on failure
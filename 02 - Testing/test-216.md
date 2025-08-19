1. Delete Buttons
    
    1. A “Delete instruction” button is added to the following pages:
        
        1. Instruction Reviewing
            
        2. Add Instruction Scope
            
        3. Ways to share the record
            
        4. Provisional Report Preview
            
    2. When the “Delete instruction” button is clicked, a modal appears, asking for confirmation to delete the instruction.
        
2. Modal
    
    1. **Modal Title:**  
        You are about to delete this instruction
        
    2. **Modal Message:**
        
        “Are you sure you wish to delete this instruction?
        
        Once deleted, the instruction cannot be recovered. A new instruction will have to be created.
        
        Information about the instruction, such as the patient details, will remain stored. Please contact us if you would like this to be removed.”
        
    3. **Buttons:**
        
        1. “Go back” - if this is clicked, close the modal.
            
        2. “Delete” - if this is clicked, the instruction is (soft) deleted from the system and the user is redirected to the Instruction Pipeline page.
            
3. Deletion Logic
    
    1. Only show the delete button if the instruction meets the following criteria:
        
        1. Instruction was created by GP surgery (NOT a client user)
            
        2. Instruction status is NOT: `Completed`, `Invoiced`, `Downloaded`, `Awaiting Approval`, `Paid`.
            
    2. If the instruction does not meet this criteria, don’t show the delete button.

## 
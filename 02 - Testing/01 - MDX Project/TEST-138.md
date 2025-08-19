## Vat_earn needs to be available on the instruction admin page 
### Steps
1. In the MDX Admin Page, Navigate to  [Instruction](https://new-qa-mdx.medi2data.com/admin/instruction/) › Instructions > Instruction you created
2. Look for a vat_earn to be associated to the instruction 


### Expected Result
The VAT earn field is associated to the instruction, is a readonly field and has a value based on 20% of the Admin fee

        

## Every time admin_fee is changed, vat_earn needs to be recalculated 
### Steps
1. In the MDX Admin Page, Navigate to  [Instruction](https://new-qa-mdx.medi2data.com/admin/instruction/) › Instructions > Instruction you created
2. Look for a vat_earn to be associated to the instruction and check the value
3. Update the admin fee associated to the instruction and press <Save>
4. Re-open the instruction and confirm that the vat_earn fee has been updated

### Expected Result
the vat_earn fee has been updated according to the value of admin_fee

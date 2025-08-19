# TEST-247

## Confirm that an instruction can be created that has a snomed code longer than default JavaScript int length

### Steps
1. Create a Template from MDX admin that has the snomed code: 10692761000119107 and associate it to an organisation
2. From the client side, create an instruction that is based off of that template. 
3. Confirm that the instruction is created and has the instruction created in eMR

### Expected Results
1. The instruction can be created when the snomed code is longer than the default JS int
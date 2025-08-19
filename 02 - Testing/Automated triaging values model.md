As a developer I need to keep track of all predictions our triaging AI models make. I want to use these in future for analysing the success of the model behaviour as well as sharing the triaging results to hubspot.

# Have a model for capturing field name, field value, confidence rating and the pre-instruction it belongs to
## Confirm that there is model that captures the classifications for the pre-instructions
### Steps
1. Examples:
        
        1. {field_name: report_type, field_value: “UC”, confidence: 0.93, pre_instruction_id=2}
            
        2. {field_name: patient_dob, field_value: “1999-04-03”, confidence: 0.23, pre_instruction_id=2}
            
2. The model will be used to store results from the triaging workflows and create notes for hubspot
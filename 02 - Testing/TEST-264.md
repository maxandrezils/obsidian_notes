- Emis and Vision Event Writeback Test-265
	## Scenarios
	allow for medical record writeback for vision and emis IM1 on ALL report types
	ENABLE_IM1_WRITEBACK_FLAG should still be a feature flag for controlling the functionality
	Writeback should occur on completion of the final report.
	There is no change to the record text written back to the clinical systems.

	### Writeback occurs for vision reports when the flag is enabled
	#### Steps:
	1. While the ENABLE_IM1_WRITEBACK_FLAG is set to true, create a vision report
	2. Progress the report to Completed and confirm that the writeback has occured for the date you completed the report on 


	### Writeback occurs for EEMIS IM1 reports when the flag is enabled
	#### Steps:
	1. While the ENABLE_IM1_WRITEBACK_FLAG is set to true, create a EMIS IM 1 report
	2. Progress the report to Completed and confirm that the writeback has occured for the date you completed the report on 
	
	### Writeback does not occur for vision reports when the flag is disabled
	#### Steps:
	1. While the ENABLE_IM1_WRITEBACK_FLAG is set to false, create a vision report
	2. Progress the report to Completed and confirm that the writeback has not occured for the date you completed the report on 


	### Writeback occurs for EEMIS IM1 reports when the flag is enabled
	#### Steps:
	1. While the ENABLE_IM1_WRITEBACK_FLAG is set to false, create a EMIS IM 1 report
	2. Progress the report to Completed and confirm that the writeback has not occured for the date you completed the report on 
	
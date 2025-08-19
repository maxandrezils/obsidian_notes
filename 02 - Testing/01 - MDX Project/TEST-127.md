---
state: Final
---
# Scenario 1
	Confirm that the rejection mail is no longer sent to the GP if the instruction is marked as rejected in EMR Admin
	
	## Steps
	- Create a new instruction in MDX
	- In EMR Admin, mark the instruction as rejected
	- Confirm that you do not receive the rejection email
	- Create a new instruction in EMR
	- In EMR Admin, mark the instruction as rejected
	- Confirm that you do not receive the rejection email

## Expected Result
- The GP user should not receive the rejection email
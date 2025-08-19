
#### **AC**

### Terraform successfully removes the `preparing` service without affecting other Celery workers.
- Confirm that the celery workers were not affected by the terraform change
	- This will be done by running redactions and confirming with devops that nothing has changed on that front
	- Compare QA to UAT by doing the same manual redactions in both environments
- `finalising` service successfully runs `preparing`queue and processes tasks.
    - This will be done by running redactions and confirming with devops that nothing has changed on that front
    - Compare QA to UAT by doing the same manual redactions in both environments
- System performance remains stable post-migration.
	  Confirm that performance does not degrade by running automation with @redaction tag before and after the change
4. Logging and monitoring are updated to reflect the queue changes.
	 - re-enable logs on qa for the test and review the logs, @deg and @emily to assist here   
5. No impact on end-user experience.
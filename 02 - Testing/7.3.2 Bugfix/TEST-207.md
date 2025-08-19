### Acceptance Criteria  
- The time between clicking “Save” on an attachment and the next one being ready for review is significantly reduced.
- On the save of the attachment, do a post, wait for that post to complete, then redirect, then load the next view.
- Attachments are saved asynchronously, allowing for the clinician to immediately transition to the next attachment without waiting.
- Ensure that the system redirects to the next attachment view as soon as the save operation is initiated, without waiting for the save to complete.

Note: we need to check what happens if the connection is interrupted or the user closes the tab
## The time between clicking “Save” on an attachment and the next one being ready for review is significantly reduced.

### Steps
1. In QA, Generate an instruction and proceed to the provisional report screen
2. Open the attachment editing screen
3. Open developer tools > Network and Update the redacted items associated to the attachment and press [Save Changes]
4. Confirm that you see the Attachment redaction prompt
5. Press [Continue]

---

### Expected Results
1. The Attachment redaction should have the following copy:
	We have identified this attachment is a large file, and therefore, we will process in the background and let you know when it is complete. You can continue with other attachments in the meantime. Clicking Continue will return to other attachment or provisional report.
2. The page should save and the update of pdf redactions should complete in the background.
3. The next attachment in the list should be navigated to after pressing [Continue]

## Pressing the Cancel button should not update the attachment redactions

### Steps
1. In QA, Generate an instruction and proceed to the provisional report screen
2. Open the attachment editing screen and  Update the redacted items associated to the attachment and press [Save Changes]
3. On the Attachment redaction prompt, press [Cancel]
4. Confirm that the redactions are not updated.

### Expected Results
the redactions should not be updated





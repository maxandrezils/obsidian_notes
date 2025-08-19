**Description:**  
Design and implement a reusable, scalable model for attaching one or more **supporting documents** to an `Instruction`. This model must support a wide variety of document types, not limited to Bupa onset forms, and must allow up to 5 associated files per instruction (this number may change in the furture). These documents may be generated internally (e.g. form outputs) or uploaded by external/internal users.

Goals:
- Allow 1–5 documents to be attached to a single `Instruction`that are not the final report
- Support structured metadata (type, upload source, timestamp)
- Enable future UI filtering/grouping (e.g. system-generated vs uploaded)
- Not tied to Bupa or any specific client/flow
    

### Functional Requirements:

#### A. Relationships
- Each `Instruction` can have multiple `SupportingDocument` objects (up to 5).
- A document must be linked to a valid instruction.
- `related_name="supporting_documents"` allows reverse lookup from `Instruction`.
    

#### B. File Handling
- Uploaded files should use the existing secure file storage setup.
- `upload_to` path should reflect instruction ID and timestamp.
- Enforce file type and size validation (PDF, DOCX, max 15MB each, backend-side).
    

#### C. Metadata & Audit
- Track who uploaded/generated the file (`uploaded_by`)
- Include `source` (user vs system) to support filtering
- Automatically timestamp each document
    

#### D. Validation Rules
- No more than 5 documents per instruction
    
- `document_type` must be selected and unique per type if applicable (e.g. only one Bupa onset form per instruction)
    
- Required fields: `file`, `document_type`, `instruction`, `source`
    

### Acceptance Criteria:

- A new `SupportingDocument` model exists with appropriate fields and constraints
    
- One-to-many relation to `Instruction` is functional and testable
    
- File upload path uses instruction ID and timestamp
    
- New admin interface or API endpoint to view and manage supporting documents per instruction
    
- Documents appear in the audit trail/log
    
- File validations (type, size, count) are enforced at the backend
    
- Bupa onset PDF can be attached using this structure without needing special handling
    

## Tempo
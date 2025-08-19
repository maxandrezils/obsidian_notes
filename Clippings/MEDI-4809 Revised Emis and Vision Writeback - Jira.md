---
title: "[MEDI-4809] Revised: Emis and Vision Writeback - Jira"
source: "https://medi2data.atlassian.net/browse/MEDI-4809"
author:
  - "[[JIRA]]"
published:
created: 2024-11-13
description:
tags:
  - "clippings"
---
# MEDI-4809 Revised Emis and Vision Writeback - Jira
1. `ENABLE_IM1_WRITEBACK_FLAG` is a feature flag for controlling the functionality.
2. The write back happens for ALL report types for Vision and EMIS EM1.
3. There is no change to the record text written back to the clinical systems.
4. Write back occurs on the completion of the final report.
5. Write back ONLY occurs for the PREVIEW of the final report. It does NOT contain attachments.
6. Write back flag
    1. If a report has been **successfully** written back, add a flag indicating success.
    2. If a report was **unable** to be written back, add an flag indicating failure.
    3. There should also be an option **none**, for when no write back has occurred yet.


## The Write back Happens for ALL Report Types for Vision
### Steps
1. Create a SAR report and transition it to the preview stage
2. Create another SAR report and confirm that the writeback has occurred and appears in the preview of the new report

## The Write back Happens for ALL Report Types for EMIS
### Steps
1. Create a SAR report and transition it to the preview stage
2. Create another SAR report and confirm that the writeback has occurred and appears in the preview of the new report

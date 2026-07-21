---
title: "Week 8 Worklog"
date: 2026-06-08
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Understand automated video processing status updates.
* Describe how EventBridge captures MediaConvert events and triggers Lambda.
* Review the backend webhook that updates episode status in RDS.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Record the EventBridge rule netflop-mediaconvert-job-state-change | 06/08/2026 | 06/08/2026 | EventBridge notes |
| Tuesday | Review tracked MediaConvert statuses: COMPLETE, ERROR, and CANCELED | 06/09/2026 | 06/09/2026 | AWS Console notes |
| Wednesday | Analyze Lambda netflop-mediaconvert-notifier receiving events and calling the backend webhook | 06/10/2026 | 06/10/2026 | Lambda notes |
| Thursday | Review /api/uploads/mediaconvert/events for updating upload_status and episode readiness | 06/11/2026 | 06/11/2026 | Backend API notes |
| Friday | Record the automation benefit: admins do not need to manually sync after conversion completes | 06/12/2026 | 06/12/2026 | Test notes |
| Saturday - Sunday | Write the serverless automation section for the AWS architecture diagram | 06/13/2026 | 06/14/2026 | Report draft |

### Week 8 Achievements:

* Described the flow: MediaConvert -> EventBridge -> Lambda -> Backend webhook -> RDS.
* Understood that Lambda is used for small automated tasks, not as a replacement for the main backend.
* Completed the video status automation section.

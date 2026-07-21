---
title: "Week 2 Worklog"
date: 2026-04-27
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Strengthen AWS fundamentals needed to understand the Netflop architecture.
* Build the high-level architecture flow for users, admins, and media processing.
* Identify the role of each AWS service in the system.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Review Region, Availability Zone, IAM, EC2, RDS, S3, and CloudFront concepts | 04/27/2026 | 04/27/2026 | AWS Documentation |
| Tuesday | Draw the main flow: User/Admin -> Cloudflare -> EC2/Nginx -> React/Node.js -> RDS MySQL | 04/28/2026 | 04/28/2026 | Netflop architecture notes |
| Wednesday | Analyze the admin upload flow from backend to S3 input and MediaConvert job creation | 04/29/2026 | 04/29/2026 | Project notes |
| Thursday | Analyze the HLS playback flow from S3 output through CloudFront to the video player | 04/30/2026 | 04/30/2026 | AWS Media Services |
| Friday | Study the automation flow: EventBridge, Lambda notifier, backend webhook, and episode status update | 05/01/2026 | 05/01/2026 | EventBridge/Lambda notes |
| Saturday - Sunday | Prepare the first high-level AWS architecture diagram for the proposal and report | 05/02/2026 | 05/03/2026 | Draw.io/Markdown notes |

### Week 2 Achievements:

* Understood the overall Netflop architecture for both the main web flow and the media pipeline.
* Understood why EC2 runs the main application while Lambda handles small automated tasks.
* Prepared the first draft of the AWS architecture diagram.

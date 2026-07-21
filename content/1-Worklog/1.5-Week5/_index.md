---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Understand how Amazon S3 stores videos, HLS output, images, avatars, and subtitles.
* Clearly separate the input bucket and output bucket roles.
* Prepare the media upload flow for the report.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Record the main buckets: netflop-input-source and netflop-output-source | 05/18/2026 | 05/18/2026 | AWS Console notes |
| Tuesday | Analyze the input bucket role for original uploads, video input, and subtitle input | 05/19/2026 | 05/19/2026 | S3 notes |
| Wednesday | Analyze the output bucket role for HLS output, public images, avatars, and VTT subtitles | 05/20/2026 | 05/20/2026 | S3 notes |
| Thursday | Review object naming for videos, posters, avatars, and subtitles | 05/21/2026 | 05/21/2026 | Backend upload notes |
| Friday | Study S3 access policy, block public access, and IAM permissions for EC2, Lambda, and MediaConvert | 05/22/2026 | 05/22/2026 | IAM/S3 Policy |
| Saturday - Sunday | Write the S3 architecture section and prepare the media flow illustration | 05/23/2026 | 05/24/2026 | Report draft |

### Week 5 Achievements:

* Understood that S3 is the central storage layer for Netflop media data.
* Clearly separated original input data from user-facing output data.
* Prepared content for explaining video, image, avatar, and subtitle uploads.

---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Understand subtitle, image, and avatar handling in Netflop.
* Describe the Lambda function that converts SRT subtitles to VTT.
* Review how the backend stores media URLs in the database.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Survey admin subtitle upload for .vtt and .srt files | 06/15/2026 | 06/15/2026 | Admin notes |
| Tuesday | Analyze the .vtt flow stored directly in S3 output for the video player | 06/16/2026 | 06/16/2026 | S3 notes |
| Wednesday | Analyze the .srt flow uploaded to S3 input under subtitle-input/ | 06/17/2026 | 06/17/2026 | Backend notes |
| Thursday | Study Lambda netflop-subtitle-converter that converts .srt to .vtt and saves it to S3 output | 06/18/2026 | 06/18/2026 | Lambda notes |
| Friday | Review movie image and user avatar uploads to S3 and URL storage in RDS | 06/19/2026 | 06/19/2026 | Upload API notes |
| Saturday - Sunday | Write the supporting media management section for subtitles, posters, and avatars | 06/20/2026 | 06/21/2026 | Report draft |

### Week 9 Achievements:

* Understood how the system supports both direct VTT subtitles and SRT subtitles that need conversion.
* Described the subtitle converter Lambda function and its value for admin workflow.
* Completed the report content about images, avatars, and subtitles.

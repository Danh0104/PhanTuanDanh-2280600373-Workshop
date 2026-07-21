---
title: "Week 6 Worklog"
date: 2026-05-25
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Study and describe video processing with AWS Elemental MediaConvert.
* Understand how MP4/MKV videos are converted into multi-quality HLS output.
* Review the metadata saved by the backend after creating a convert job.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Learn HLS concepts: .m3u8 files, segments, and adaptive streaming | 05/25/2026 | 05/25/2026 | MediaConvert docs |
| Tuesday | Analyze the admin multipart video upload flow to the backend | 05/26/2026 | 05/26/2026 | Upload API notes |
| Wednesday | Record how the backend uploads video to S3 input and creates a MediaConvert job | 05/27/2026 | 05/27/2026 | Backend/AWS notes |
| Thursday | Review HLS output qualities: 360p, 480p, 720p, and 1080p | 05/28/2026 | 05/28/2026 | MediaConvert output |
| Friday | Analyze jobId, hls_url, cloudfront_url, and upload_status saved in the database | 05/29/2026 | 05/29/2026 | RDS/API notes |
| Saturday - Sunday | Write the video conversion workflow and processing status section | 05/30/2026 | 05/31/2026 | Report draft |

### Week 6 Achievements:

* Understood MediaConvert's role in converting uploaded videos into HLS for web playback.
* Described the process from admin upload to ready HLS output.
* Prepared the explanation for why video processing is separated from the main application.

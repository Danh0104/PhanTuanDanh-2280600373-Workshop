---
title: "Week 7 Worklog"
date: 2026-06-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Understand CloudFront distribution for HLS streaming.
* Record the protected streaming mechanism using signed cookies.
* Test how the player receives the stream URL through the backend.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Record CloudFront distributions and enabled/disabled status | 06/01/2026 | 06/01/2026 | AWS Console notes |
| Tuesday | Analyze d11jdx7259stge.cloudfront.net as the protected HLS streaming distribution | 06/02/2026 | 06/02/2026 | CloudFront notes |
| Wednesday | Study how CloudFront caches .m3u8 files and segments from S3 output | 06/03/2026 | 06/03/2026 | CloudFront docs |
| Thursday | Review the /api/stream/session API that issues CloudFront signed cookies | 06/04/2026 | 06/04/2026 | Backend API notes |
| Friday | Test frontend flow: fetch movie/episode data from backend and play HLS in the video player | 06/05/2026 | 06/05/2026 | Test notes |
| Saturday - Sunday | Write the protected streaming and content distribution section | 06/06/2026 | 06/07/2026 | Report draft |

### Week 7 Achievements:

* Understood how CloudFront reduces S3 load and improves video delivery.
* Understood how the system grants stream access through signed cookies instead of exposing files publicly.
* Prepared the report content for the movie playback flow.

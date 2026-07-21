---
title: "Worklog"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

This section presents my internship worklog over 12 weeks, from **April 19, 2026** to **July 11, 2026**. The worklog follows a practical internship flow: learning AWS fundamentals, studying the Netflop web system, analyzing its architecture, documenting the media pipeline, reviewing monitoring/security, and completing the final report.

Netflop is a movie streaming website deployed on AWS with the main flow:

**User/Admin -> Cloudflare DNS/HTTPS -> EC2/Nginx -> React frontend + Node.js API -> RDS MySQL**

The media processing flow is separated:

**Admin uploads video -> EC2 backend -> S3 input -> MediaConvert -> S3 output -> CloudFront -> Video player**

The system also uses EventBridge, Lambda, CloudWatch, SNS, IAM, and Systems Manager for automation, monitoring, access control, and deployment support.

The weekly contents are:

**Week 1:** [Surveying the Netflop project and defining the report scope](1.1-week1/)

**Week 2:** [Learning AWS fundamentals and the overall system architecture](1.2-week2/)

**Week 3:** [Studying the web application, backend API, and database](1.3-week3/)

**Week 4:** [Analyzing EC2, Nginx, domain, and access security](1.4-week4/)

**Week 5:** [Designing the media storage flow with Amazon S3](1.5-week5/)

**Week 6:** [Integrating MediaConvert for HLS video processing](1.6-week6/)

**Week 7:** [Deploying CloudFront and protected streaming access](1.7-week7/)

**Week 8:** [Automating video status updates with EventBridge and Lambda](1.8-week8/)

**Week 9:** [Handling subtitles, images, and avatars with S3/Lambda](1.9-week9/)

**Week 10:** [Monitoring the system with CloudWatch, SNS, and operational testing](1.10-week10/)

**Week 11:** [Consolidating the AWS architecture, risks, and optimization directions](1.11-week11/)

**Week 12:** [Finalizing the report, reviewing content, and preparing submission](1.12-week12/)
#### github
https://github.com/Danh0104/Web-xem-phim-Netflop.git
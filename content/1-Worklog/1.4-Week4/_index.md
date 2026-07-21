---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Analyze the EC2 infrastructure running the main application.
* Understand the role of Nginx, Cloudflare domain, and security groups.
* Record deployment security improvements for the report.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Record EC2 information: netflop-web, t3.micro instance type, public IP, and security group | 05/11/2026 | 05/11/2026 | AWS Console notes |
| Tuesday | Study how Nginx reverse proxy serves the React frontend and forwards API requests to Node.js | 05/12/2026 | 05/12/2026 | Nginx notes |
| Wednesday | Review Cloudflare's role in DNS, HTTPS, and access through the netflop.win domain | 05/13/2026 | 05/13/2026 | Cloudflare notes |
| Thursday | Review required ports for web traffic, SSH/deployment, and backend connection to RDS | 05/14/2026 | 05/14/2026 | Security Group |
| Friday | Study deployment/reload support on EC2 through AWS Systems Manager and local AWS CLI | 05/15/2026 | 05/15/2026 | SSM notes |
| Saturday - Sunday | Record the RDS public accessibility risk and propose limiting access to the EC2 security group | 05/16/2026 | 05/17/2026 | Best practices |

### Week 4 Achievements:

* Described EC2 as the main application host for frontend build, Node.js backend, and Nginx.
* Understood how Cloudflare handles domain and HTTPS access for users.
* Identified security improvement points for the final evaluation section.

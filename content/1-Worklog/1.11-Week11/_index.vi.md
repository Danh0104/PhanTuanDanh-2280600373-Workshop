---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 1
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Tổng hợp kiến trúc AWS hoàn chỉnh của Netflop.
* Đánh giá ưu điểm, hạn chế và hướng hoàn thiện hệ thống.
* Chuẩn bị nội dung cho Proposal, Workshop, Self-evaluation và phần kết luận.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Hoàn thiện sơ đồ kiến trúc chính: User/Admin, Cloudflare, EC2, Nginx, React, Node.js, RDS | 29/06/2026 | 29/06/2026 | Architecture diagram |
| 3 | Hoàn thiện sơ đồ media pipeline: S3 input, MediaConvert, S3 output, CloudFront và Video Player | 30/06/2026 | 30/06/2026 | Architecture diagram |
| 4 | Hoàn thiện sơ đồ automation: EventBridge, Lambda notifier, backend webhook và RDS | 01/07/2026 | 01/07/2026 | Architecture diagram |
| 5 | Bổ sung ghi chú về IAM Role, Systems Manager, CloudWatch, SNS và Cognito cần xác nhận account/region | 02/07/2026 | 02/07/2026 | AWS notes |
| 6 | Viết phần đánh giá rủi ro: RDS public accessible, phân quyền S3, bảo vệ stream và kiểm soát chi phí | 03/07/2026 | 03/07/2026 | Best practices |
| 7 - Chủ nhật | Rà soát tính logic giữa Worklog, Proposal, Workshop và Self-evaluation | 04/07/2026 | 05/07/2026 | Báo cáo nháp |

### Kết quả đạt được tuần 11:

* Có bản mô tả kiến trúc AWS tương đối đầy đủ cho web Netflop.
* Xác định được các điểm mạnh của hệ thống: tách media pipeline, dùng CloudFront, tự động hóa bằng Lambda/EventBridge và có monitoring.
* Chuẩn bị được phần đề xuất cải thiện bảo mật, chi phí và vận hành.

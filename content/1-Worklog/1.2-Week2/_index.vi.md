---
title: "Worklog Tuần 2"
date: 2026-04-27
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Củng cố kiến thức AWS nền tảng để đọc hiểu kiến trúc Netflop.
* Xây dựng sơ đồ tổng quan cho luồng người dùng, admin và xử lý media.
* Nhận diện vai trò của từng dịch vụ AWS trong hệ thống.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Ôn lại các khái niệm cơ bản về Region, Availability Zone, IAM, EC2, RDS, S3 và CloudFront | 27/04/2026 | 27/04/2026 | AWS Documentation |
| 3 | Vẽ luồng tổng quan User/Admin -> Cloudflare -> EC2/Nginx -> React/Node.js -> RDS MySQL | 28/04/2026 | 28/04/2026 | Tài liệu kiến trúc Netflop |
| 4 | Phân tích luồng upload video từ admin lên S3 input và tạo job MediaConvert | 29/04/2026 | 29/04/2026 | Ghi chú dự án |
| 5 | Phân tích luồng phát video HLS từ S3 output qua CloudFront đến video player | 30/04/2026 | 30/04/2026 | AWS Media Services |
| 6 | Ghi nhận luồng tự động hóa: EventBridge, Lambda notifier, backend webhook và cập nhật trạng thái tập phim | 01/05/2026 | 01/05/2026 | EventBridge/Lambda notes |
| 7 - Chủ nhật | Tổng hợp sơ đồ kiến trúc mức cao để dùng cho phần Proposal và báo cáo | 02/05/2026 | 03/05/2026 | Draw.io/Markdown notes |

### Kết quả đạt được tuần 2:

* Nắm được kiến trúc tổng quan của Netflop theo cả luồng web chính và luồng media.
* Hiểu được vì sao hệ thống dùng EC2 cho ứng dụng chính, còn Lambda chỉ xử lý các tác vụ tự động nhỏ.
* Có bản nháp sơ đồ AWS Architecture đầu tiên cho báo cáo.

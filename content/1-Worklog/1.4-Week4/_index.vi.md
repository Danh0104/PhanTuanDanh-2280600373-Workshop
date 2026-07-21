---
title: "Worklog Tuần 4"
date: 2026-05-11
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Phân tích hạ tầng chạy ứng dụng chính trên EC2.
* Tìm hiểu vai trò của Nginx, Cloudflare domain và security group.
* Ghi nhận các điểm cần cải thiện về bảo mật triển khai.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Ghi nhận thông tin EC2 netflop-web, instance type t3.micro, public IP và security group | 11/05/2026 | 11/05/2026 | AWS Console notes |
| 3 | Tìm hiểu cách Nginx reverse proxy phục vụ React frontend và chuyển tiếp request đến Node.js backend | 12/05/2026 | 12/05/2026 | Nginx config notes |
| 4 | Kiểm tra vai trò Cloudflare trong DNS, HTTPS và truy cập qua domain netflop.win | 13/05/2026 | 13/05/2026 | Cloudflare notes |
| 5 | Rà soát các cổng cần mở cho web, SSH/deploy và kết nối backend với RDS | 14/05/2026 | 14/05/2026 | Security Group |
| 6 | Tìm hiểu cách deploy/reload EC2 bằng AWS Systems Manager từ local AWS CLI | 15/05/2026 | 15/05/2026 | SSM notes |
| 7 - Chủ nhật | Ghi nhận rủi ro: RDS public accessible và đề xuất giới hạn security group chỉ cho EC2 truy cập | 16/05/2026 | 17/05/2026 | Best practices |

### Kết quả đạt được tuần 4:

* Mô tả được vai trò của EC2 là nơi chạy ứng dụng chính, gồm frontend build, backend Node.js và Nginx.
* Hiểu được Cloudflare đang xử lý domain và HTTPS phía người dùng.
* Ghi nhận được các điểm cải thiện bảo mật để đưa vào phần đánh giá cuối báo cáo.

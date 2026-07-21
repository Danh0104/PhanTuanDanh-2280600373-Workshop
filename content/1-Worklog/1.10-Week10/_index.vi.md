---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 1
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Tìm hiểu monitoring và cảnh báo vận hành cho Netflop.
* Ghi nhận các CloudWatch alarms liên quan đến EC2, RDS và Lambda.
* Kiểm thử các luồng chính để đánh giá độ ổn định của hệ thống.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Ghi nhận CloudWatch theo dõi EC2 CPU, memory, disk và status check | 22/06/2026 | 22/06/2026 | CloudWatch notes |
| 3 | Ghi nhận CloudWatch theo dõi RDS CPU, connections, free storage và freeable memory | 23/06/2026 | 23/06/2026 | RDS monitoring |
| 4 | Kiểm tra alarm Lambda errors cho netflop-mediaconvert-notifier và netflop-subtitle-converter | 24/06/2026 | 24/06/2026 | Lambda monitoring |
| 5 | Tìm hiểu SNS topic netflop-alerts dùng để gửi cảnh báo khi hệ thống có bất thường | 25/06/2026 | 25/06/2026 | SNS notes |
| 6 | Kiểm thử các luồng chính: đăng nhập, xem phim, upload video, convert, phát HLS, upload phụ đề, đổi avatar | 26/06/2026 | 26/06/2026 | Test checklist |
| 7 - Chủ nhật | Tổng hợp lỗi, giới hạn và đề xuất cải thiện khả năng quan sát hệ thống | 27/06/2026 | 28/06/2026 | Báo cáo nháp |

### Kết quả đạt được tuần 10:

* Mô tả được vai trò CloudWatch và SNS trong việc theo dõi sức khỏe hệ thống.
* Có checklist kiểm thử các chức năng quan trọng của Netflop.
* Ghi nhận được các điểm cần theo dõi khi hệ thống phục vụ nhiều người dùng hơn.

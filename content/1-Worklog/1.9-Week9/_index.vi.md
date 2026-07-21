---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Tìm hiểu luồng xử lý phụ đề, ảnh và avatar của Netflop.
* Mô tả Lambda chuyển đổi phụ đề SRT sang VTT.
* Kiểm tra cách backend lưu URL media vào database.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Khảo sát chức năng admin upload phụ đề .vtt hoặc .srt cho tập phim | 15/06/2026 | 15/06/2026 | Admin notes |
| 3 | Phân tích luồng .vtt lưu trực tiếp vào S3 output để video player đọc phụ đề | 16/06/2026 | 16/06/2026 | S3 notes |
| 4 | Phân tích luồng .srt upload vào S3 input dưới thư mục subtitle-input/ | 17/06/2026 | 17/06/2026 | Backend notes |
| 5 | Tìm hiểu Lambda netflop-subtitle-converter chuyển .srt thành .vtt và lưu về S3 output | 18/06/2026 | 18/06/2026 | Lambda notes |
| 6 | Khảo sát chức năng upload ảnh phim và avatar người dùng lên S3, sau đó lưu URL vào RDS | 19/06/2026 | 19/06/2026 | Upload API notes |
| 7 - Chủ nhật | Viết phần mô tả quản lý media phụ trợ gồm subtitle, poster và avatar | 20/06/2026 | 21/06/2026 | Báo cáo nháp |

### Kết quả đạt được tuần 9:

* Hiểu được cách hệ thống hỗ trợ cả phụ đề VTT trực tiếp và SRT cần chuyển đổi.
* Mô tả được vai trò của Lambda subtitle converter trong việc giảm thao tác thủ công cho admin.
* Hoàn thiện nội dung về quản lý ảnh, avatar và phụ đề trong báo cáo.


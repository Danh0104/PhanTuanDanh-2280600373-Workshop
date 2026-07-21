---
title: "Worklog Tuần 3"
date: 2026-05-04
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Khảo sát phần ứng dụng của Netflop: frontend, backend API và database.
* Hiểu cách dữ liệu phim, tập phim, người dùng và lịch sử xem được lưu trữ.
* Chuẩn bị nội dung mô tả nghiệp vụ cho báo cáo.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Kiểm tra giao diện React frontend và các màn hình chính dành cho người dùng | 04/05/2026 | 04/05/2026 | Source/frontend notes |
| 3 | Khảo sát backend Node.js API: route phim, tập phim, upload, user, rating, comment và streaming session | 05/05/2026 | 05/05/2026 | Source/backend notes |
| 4 | Liệt kê các bảng dữ liệu chính trong RDS MySQL: tài khoản, phim, tập phim, phụ đề, lịch sử xem, yêu thích, đánh giá, bình luận | 06/05/2026 | 06/05/2026 | Database notes |
| 5 | Phân tích cách backend lưu jobId, hls_url, cloudfront_url và upload_status khi admin upload phim | 07/05/2026 | 07/05/2026 | Upload API |
| 6 | Ghi nhận các API liên quan đến tiếp tục xem, avatar và metadata phim | 08/05/2026 | 08/05/2026 | Backend API |
| 7 - Chủ nhật | Viết bản nháp mô tả chức năng web tương ứng với các thành phần AWS | 09/05/2026 | 10/05/2026 | Báo cáo nháp |

### Kết quả đạt được tuần 3:

* Hiểu được mối liên hệ giữa nghiệp vụ website xem phim và dữ liệu lưu trong RDS MySQL.
* Xác định được các API quan trọng cần nhắc trong báo cáo, đặc biệt là upload video và cấp phiên stream.
* Có nội dung nền để giải thích vì sao kiến trúc AWS hiện tại phù hợp với hệ thống Netflop.


---
title: "Worklog Tuần 7"
date: 2026-06-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Tìm hiểu CloudFront trong việc phân phối HLS stream cho người dùng.
* Ghi nhận cơ chế bảo vệ stream bằng signed cookies.
* Kiểm thử luồng player nhận URL phát video qua backend.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Ghi nhận các CloudFront distribution đang dùng và trạng thái enabled/disabled | 01/06/2026 | 01/06/2026 | AWS Console notes |
| 3 | Phân tích distribution d11jdx7259stge.cloudfront.net phục vụ HLS stream được bảo vệ | 02/06/2026 | 02/06/2026 | CloudFront notes |
| 4 | Tìm hiểu cách CloudFront cache file .m3u8 và segment từ S3 output bucket | 03/06/2026 | 03/06/2026 | CloudFront docs |
| 5 | Kiểm tra API /api/stream/session cấp CloudFront signed cookies cho phiên xem video | 04/06/2026 | 04/06/2026 | Backend API notes |
| 6 | Thử luồng frontend gọi backend lấy thông tin phim/tập và phát HLS bằng video player | 05/06/2026 | 05/06/2026 | Test notes |
| 7 - Chủ nhật | Viết phần mô tả bảo vệ stream và phân phối nội dung trong báo cáo | 06/06/2026 | 07/06/2026 | Báo cáo nháp |

### Kết quả đạt được tuần 7:

* Hiểu được CloudFront giúp giảm tải cho S3 và cải thiện tốc độ phát video.
* Nắm được cách hệ thống cấp quyền xem stream qua signed cookies thay vì mở public trực tiếp.
* Có nội dung để trình bày luồng phát phim từ backend đến video player.


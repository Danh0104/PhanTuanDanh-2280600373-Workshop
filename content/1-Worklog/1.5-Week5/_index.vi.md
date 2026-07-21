---
title: "Worklog Tuần 5"
date: 2026-05-18
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Tìm hiểu vai trò Amazon S3 trong lưu trữ video, HLS output, ảnh, avatar và phụ đề.
* Phân tách rõ input bucket và output bucket trong kiến trúc.
* Chuẩn bị mô tả luồng upload media cho báo cáo.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Ghi nhận các bucket chính: netflop-input-source và netflop-output-source | 18/05/2026 | 18/05/2026 | AWS Console notes |
| 3 | Phân tích vai trò bucket input trong lưu file gốc upload, video input và subtitle input | 19/05/2026 | 19/05/2026 | S3 notes |
| 4 | Phân tích vai trò bucket output trong lưu HLS output, ảnh public, avatar và phụ đề VTT | 20/05/2026 | 20/05/2026 | S3 notes |
| 5 | Kiểm tra naming convention cho object video, poster, avatar và subtitle | 21/05/2026 | 21/05/2026 | Backend upload notes |
| 6 | Tìm hiểu chính sách truy cập S3, block public access và quyền IAM cho EC2/Lambda/MediaConvert | 22/05/2026 | 22/05/2026 | IAM/S3 Policy |
| 7 - Chủ nhật | Viết phần mô tả S3 trong kiến trúc Netflop và chuẩn bị hình minh họa luồng media | 23/05/2026 | 24/05/2026 | Báo cáo nháp |

### Kết quả đạt được tuần 5:

* Hiểu được S3 là thành phần lưu trữ trung tâm cho toàn bộ dữ liệu media của Netflop.
* Phân biệt rõ dữ liệu gốc ở input bucket và dữ liệu phục vụ người dùng ở output bucket.
* Có nội dung để trình bày luồng upload video, ảnh, avatar và phụ đề trong báo cáo.


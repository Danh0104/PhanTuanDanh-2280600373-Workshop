---
title: "Worklog Tuần 6"
date: 2026-05-25
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Tìm hiểu và mô tả luồng xử lý video bằng AWS Elemental MediaConvert.
* Nắm cách hệ thống chuyển video MP4/MKV thành HLS nhiều chất lượng.
* Kiểm tra các thông tin backend lưu lại sau khi tạo job convert.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Tìm hiểu khái niệm HLS, file .m3u8, segment và adaptive streaming | 25/05/2026 | 25/05/2026 | AWS MediaConvert docs |
| 3 | Phân tích luồng admin upload video MP4/MKV lên backend qua multipart request | 26/05/2026 | 26/05/2026 | Upload API notes |
| 4 | Ghi nhận cách backend upload video lên S3 input bucket và tạo MediaConvert job | 27/05/2026 | 27/05/2026 | Backend/AWS notes |
| 5 | Kiểm tra output HLS gồm các quality 360p, 480p, 720p và 1080p | 28/05/2026 | 28/05/2026 | MediaConvert output |
| 6 | Phân tích các trường jobId, hls_url, cloudfront_url và upload_status lưu trong database | 29/05/2026 | 29/05/2026 | RDS/API notes |
| 7 - Chủ nhật | Viết phần mô tả quy trình convert video và các trạng thái xử lý trong báo cáo | 30/05/2026 | 31/05/2026 | Báo cáo nháp |

### Kết quả đạt được tuần 6:

* Hiểu được vai trò MediaConvert trong việc chuẩn hóa video đầu vào thành HLS để phát trên web.
* Mô tả được quá trình từ admin upload đến khi hệ thống có file HLS sẵn sàng.
* Chuẩn bị được nội dung giải thích tại sao xử lý video được tách khỏi ứng dụng chính.


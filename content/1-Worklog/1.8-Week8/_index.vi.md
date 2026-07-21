---
title: "Worklog Tuần 8"
date: 2026-06-08
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Tìm hiểu cơ chế tự động cập nhật trạng thái xử lý video.
* Mô tả luồng EventBridge bắt sự kiện MediaConvert và kích hoạt Lambda.
* Kiểm tra webhook backend cập nhật trạng thái tập phim trong RDS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Ghi nhận rule EventBridge netflop-mediaconvert-job-state-change | 08/06/2026 | 08/06/2026 | EventBridge notes |
| 3 | Kiểm tra các trạng thái MediaConvert được theo dõi: COMPLETE, ERROR và CANCELED | 09/06/2026 | 09/06/2026 | AWS Console notes |
| 4 | Phân tích Lambda netflop-mediaconvert-notifier nhận event và gọi webhook backend | 10/06/2026 | 10/06/2026 | Lambda notes |
| 5 | Kiểm tra endpoint /api/uploads/mediaconvert/events dùng để cập nhật upload_status và trạng thái tập phim | 11/06/2026 | 11/06/2026 | Backend API notes |
| 6 | Ghi nhận lợi ích tự động hóa: admin không cần bấm sync thủ công sau khi convert hoàn tất | 12/06/2026 | 12/06/2026 | Test notes |
| 7 - Chủ nhật | Viết phần serverless automation trong sơ đồ kiến trúc AWS | 13/06/2026 | 14/06/2026 | Báo cáo nháp |

### Kết quả đạt được tuần 8:

* Mô tả được chuỗi MediaConvert -> EventBridge -> Lambda -> Backend webhook -> RDS.
* Hiểu được vai trò Lambda trong hệ thống là xử lý tác vụ nhỏ, không thay thế backend chính.
* Hoàn thiện phần tự động hóa trạng thái video trong báo cáo.


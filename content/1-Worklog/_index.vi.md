---
title: "Nhật ký công việc"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

Trong phần này, tôi trình bày tiến độ thực tập và thực hiện báo cáo trong 12 tuần, bắt đầu từ ngày **20/04/2026** đến ngày **12/07/2026**. Nội dung worklog được xây dựng theo hướng phù hợp với sinh viên thực tập: vừa học nền tảng AWS, vừa khảo sát hệ thống web Netflop, sau đó từng bước chuẩn hóa kiến trúc, triển khai chức năng, kiểm thử, giám sát và hoàn thiện báo cáo.

Dự án Netflop là website xem phim triển khai trên AWS theo mô hình chính:

**User/Admin -> Cloudflare DNS/HTTPS -> EC2/Nginx -> React frontend + Node.js API -> RDS MySQL**

Luồng xử lý media được tách riêng:

**Admin upload video -> EC2 backend -> S3 input -> MediaConvert -> S3 output -> CloudFront -> Video player**

Ngoài ra hệ thống có các thành phần tự động hóa như EventBridge, Lambda, CloudWatch và SNS để cập nhật trạng thái xử lý video, chuyển đổi phụ đề và theo dõi vận hành.

Các nội dung chính theo từng tuần như sau:

**Tuần 1:** [Khảo sát dự án Netflop và xác định phạm vi báo cáo](1.1-week1/)

**Tuần 2:** [Tìm hiểu nền tảng AWS và kiến trúc tổng quan của hệ thống](1.2-week2/)

**Tuần 3:** [Khảo sát ứng dụng web, backend API và cơ sở dữ liệu](1.3-week3/)

**Tuần 4:** [Phân tích hạ tầng EC2, Nginx, domain và bảo mật truy cập](1.4-week4/)

**Tuần 5:** [Thiết kế luồng lưu trữ media với Amazon S3](1.5-week5/)

**Tuần 6:** [Tích hợp MediaConvert cho xử lý video HLS](1.6-week6/)

**Tuần 7:** [Triển khai CloudFront và cơ chế bảo vệ stream](1.7-week7/)

**Tuần 8:** [Tự động hóa trạng thái video bằng EventBridge và Lambda](1.8-week8/)

**Tuần 9:** [Xử lý phụ đề, hình ảnh và avatar trên S3/Lambda](1.9-week9/)

**Tuần 10:** [Theo dõi hệ thống bằng CloudWatch, SNS và kiểm thử vận hành](1.10-week10/)

**Tuần 11:** [Tổng hợp kiến trúc AWS, đánh giá rủi ro và hướng tối ưu](1.11-week11/)

**Tuần 12:** [Hoàn thiện báo cáo, rà soát nội dung và chuẩn bị nộp bài](1.12-week12/)
#### github
https://github.com/Danh0104/Web-xem-phim-Netflop.git
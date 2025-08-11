---
title : "Các bước chuẩn bị"
date :  "2025-08-05"
weight : 2
chapter : false
pre : " <b> 2.</b> "
---

{{% notice info %}}
Để thực hiện bài lab này, bạn cần chuẩn bị sẵn một Bucket S3, quyền truy cập IAM với S3 và một EC2.
{{% /notice %}}

{{% notice note %}}
Vì tôi có áp dụng đề tài này vào Project của tôi, nên bạn có thể sẽ cần phải tải thêm Project để thực hiện bài Lab này.Tải [tại đây]()
{{% /notice %}}

Trước khi bắt đầu triển khai chiến lược lưu trữ dữ liệu (Data Archival Strategy), bạn cần hoàn tất các bước chuẩn bị sau:

- Tạo một EC2 Instance .
- Tạo một Bucket S3 dùng để lưu trữ dữ liệu cần lưu trữ lâu dài.
- Tạo một User IAM có đầy đủ quyền truy cập S3.

Bạn có thể tham khảo một số bài Lab có sử dụng dịch vụ S3:

- [Làm việc với Amazon S3](https://000057.awsstudygroup.com/vi/)

### Nội dung
  - [Chuẩn bị VPC và EC2 Instance](2.1-createec2/)
  - [Tạo Bucket S3](2.2-creates3/)
  - [Tạo User IAM](2.3-createuseriam/)


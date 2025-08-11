---
title: "Thiết lập truy cập EC2"
date: "2025-08-05"
weight: 3
chapter: false
pre: " <b> 3.</b> "
---

{{% notice info %}}
Khi EC2 Instance đã được tạo, bước tiếp theo là cấu hình các cổng truy cập và cài đặt những package cần thiết.  
Việc này đảm bảo máy chủ có thể chạy Docker và triển khai RabbitMQ container một cách ổn định, sẵn sàng cho các tác vụ tiếp theo.
{{% /notice %}}


Trong phần này, chúng ta sẽ thực hiện các việc sau:

- Mở các cổng cần thiết để truy cập EC2.
- Cài đặt các package phục vụ chạy Docker.
- Thêm đường dẫn host của container vào file .env của project.


 
### Nội dung
- [Mở cổng EC2](3.1-OpenEC2Ports/)
- [Thiết lập Docker & RabbitMQ](3.2-SetupDocker&RabbitMQ/)
- [Cấu hình .env](3.3-Configure.env/)



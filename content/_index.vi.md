---
title : "Data Archival Strategy"
date :  "2025-08-08"
weight : 1
chapter : false
---

# Triển khai chiến lược lưu trữ dữ liệu với Amazon S3 và Glacier

### Tổng quan

Trong bài lab này, bạn sẽ tìm hiểu các khái niệm cơ bản và thực hành về chiến lược lưu trữ dữ liệu (Data Archival Strategy) sử dụng dịch vụ **Amazon S3** kết hợp với **S3 Glacier** và **Lifecycle Policy**. Bài lab sẽ hướng dẫn cách cấu hình tự động chuyển dữ liệu từ S3 Standard sang S3 Glacier để tối ưu hóa chi phí lưu trữ lâu dài. Bạn cũng sẽ được hướng dẫn cách kích hoạt Object Lock để bảo vệ dữ liệu không bị xóa ngoài ý muốn.


![das](images/arcdas-log.png) 

### Nội dung

 1. [Giới thiệu](1-introduce/)
 2. [Các bước chuẩn bị](2-Prerequiste/)
 3. [Thiết lập truy cập EC2](3-EC2AccessSetup/)
 4. [Cấu hình Lifecycle Policies](4-ConfigLifecyclePolicies/)
 5. [Chạy và kết quả](5-RunAndViewResults/)
 6. [Dọn dẹp tài nguyên](6-cleanup/)

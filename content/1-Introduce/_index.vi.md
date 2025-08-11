---
title: "Giới thiệu"
date: 2025-08-05
weight: 1
chapter: false
pre: "<b>1.</b>"
---

**Data Archival Strategy** là một giải pháp giúp tối ưu lưu trữ dài hạn cho các hệ thống có dữ liệu ít truy cập nhưng cần bảo tồn, chẳng hạn như blog cá nhân hoặc nền tảng nội dung số.

Trong đề tài này, tôi triển khai một chiến lược lưu trữ cho hệ thống **blog microservice** sử dụng các dịch vụ của AWS như:

- **Amazon S3 Glacier** để lưu trữ dữ liệu chi phí thấp.
- **Lifecycle Policy** để tự động hóa quá trình chuyển dữ liệu và xóa sau thời hạn.
- **Object Lock (compliance mode)** để bảo vệ nội dung không bị xóa trước khi hết thời gian giữ.

---

Với việc sử dụng các dịch vụ lưu trữ của AWS, bạn sẽ có được những **ưu điểm sau**:

- **Tiết kiệm chi phí**: Tự động chuyển bài viết cũ sang Glacier – lớp lưu trữ chi phí rẻ hơn nhiều so với S3 Standard.
- **Tự động hóa**: Dễ dàng thiết lập chính sách chuyển vùng và xóa dữ liệu không cần thiết sau thời gian định sẵn.
- **Bảo mật dữ liệu**: Với Object Lock, nội dung được bảo vệ không thể xóa sai hoặc do lỗi hệ thống trong thời gian giữ.
- **Quản lý dễ dàng**: Giao diện S3 đơn giản, không cần thêm dịch vụ quản lý trung gian.

---

Giải pháp này phù hợp với các hệ thống:

- Có khối lượng nội dung tăng theo thời gian.
- Nội dung sau một thời gian không còn chỉnh sửa, truy cập ít.
- Yêu cầu tiết kiệm tài nguyên nhưng vẫn đảm bảo khả năng phục hồi dữ liệu.
---
title: "Cấu hình Lifecycle Policies"
date: "2025-08-09"
weight: 4
chapter: false
pre: " <b> 4.</b> "
---

{{% notice info %}}
Đây là nội dung chính của Lab này, với mục tiêu cấu hình **Lifecycle Policies** cho Bucket.
Nhờ đó, các tệp dữ liệu được lưu trữ có thể tự động chuyển sang lớp lưu trữ khác, tận dụng ưu điểm riêng của từng lớp (chi phí, hiệu năng, hoặc lưu trữ lâu dài).  
Ngoài việc tự động chuyển đổi, Lifecycle Policy còn hỗ trợ nhiều tùy chọn như: xóa object, hết hạn object, hoặc quản lý phiên bản theo thời gian do chúng ta thiết lập.
{{% /notice %}}

Trong phần này, chúng ta sẽ thực hiện:
1. **Tạo Lifecycle rule**:
   - Thiết lập hành động **Transition current versions**: Chuyển kiểu lưu trữ của các phiên bản hiện tại sang lớp lưu trữ khác.
   - Thiết lập hành động **Expire current versions**: Hết hạn phiên bản hiện tại và xóa object theo thời gian định sẵn.
2. **Đặt Object Lock**: Ngăn chặn việc xóa hoặc ghi đè đối tượng trong một khoảng thời gian.
3. **Thêm khóa truy cập IAM**: Tạo khóa truy cập để sử dụng cho việc xác thực khi gửi dữ liệu từ project.

{{% notice note %}}
Ngoài 2 hành động chính trên, Lifecycle Policy còn hỗ trợ:  
\- **Transition noncurrent versions**: Chuyển các phiên bản không còn là mới nhất (noncurrent) sang lớp lưu trữ khác.  
\- **Permanently delete noncurrent versions**: Xóa vĩnh viễn các phiên bản noncurrent.  
\- **Delete expired object delete markers or incomplete multipart uploads**: Xóa delete marker đã hết hạn hoặc các phiên upload nhiều phần (multipart) chưa hoàn tất.
{{% /notice %}}


### Nội dung
 - [Tạo Lifecycle Rule](4.1-CreateLifecycleRule/)
 - [Thiết lập Object Lock](4.2-SetObjectLock/)
 - [Tạo Access Key](4.3-CreateIamAccessKey/)
---
title : "Tạo Lifecycle Rule"
date : "2024-06-08"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

### Tạo Lifecycle Rule

Trong bước này, bạn sẽ tạo một quy tắc vòng đời với 2 hành động thiết lập cho đối tượng.

1. Truy cập [AWS BUCKET](https://ap-southeast-1.console.aws.amazon.com/s3/buckets/).
   + Chọn Bucket bạn đã tạo trước đó **blog-micro-data-archive**.
   + Chuyển sang tab **Management**. 
   + Click **Create lifecycle rule** để tạo.

![lifecycle](images/4.LifecyclePolicies/001-lifecycle.png)

2. Tiếp theo: 
   + Nhập **Lifecycle rule name** là `archive-to-glacier-and-delete`.
   + Chọn phạm vi **rule scope** là **Apply to all objects in the bucket**.
   + Tích chọn ô xác nhận **I acknowledge that this rule...**.
   + Tích chọn ô **Transition current versions of objects between storage classes**.
   + Tích chọn ô **Expire current versions of objects**.
   + Tích chọn ô xác nhận **I acknowledge that this lifecycle...**.
  
![lifecycle](images/4.LifecyclePolicies/002-lifecycle.png)

3. Tiếp theo: 
   + Chọn **Choose storage class transitions** là **Glacier Flexible Retrieval (formerly Glacier)**.
   + Đặt thời gian chuyển đổi lớp lưu trữ dữ liệu sau khi đối tượng được tạo **Days after object creation**.
   + Đặt thời gian hết hạn phiên bản, tạo phiên bản được đánh dấu xóa sau khi đối tượng được tạo.
   + Click **Create rule** để tạo.

![lifecycle](images/4.LifecyclePolicies/003-lifecycle.png)
![lifecycle](images/4.LifecyclePolicies/004-lifecycle.png)
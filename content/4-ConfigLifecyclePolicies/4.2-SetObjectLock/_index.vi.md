---
title : "Thiết lập Object Lock"
date : "2024-06-08"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

### Thiết lập Object Lock

Để bảo vệ dữ liệu tránh bị xóa hay bị chỉnh sửa, bạn cần phải thiết lập khóa đối tượng cho Bucket.
1. Truy cập [Bucket](https://ap-southeast-1.console.aws.amazon.com/s3/buckets).
    + Trong Bucket, chuyển sang tab **Properties**.
    + Tìm mục **Object Lock**, click **Edit**.
    + Tại **Default retention** chọn **Enable**.
    + Tại **Default retention mode** chọn **Compliance**.
    + Đặt thời gian khóa đối tượng.
    + Click **Save changes** để lưu thay đổi.

![objlock](images/4.LifecyclePolicies/005-objlock.png)
![objlock](images/4.LifecyclePolicies/006-objlock.png)
![objlock](images/4.LifecyclePolicies/007-objlock.png)

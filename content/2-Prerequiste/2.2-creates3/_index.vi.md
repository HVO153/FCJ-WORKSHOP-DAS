---
title : "Tạo Bucket S3"
date : "2024-06-08"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

### Tạo Bucket S3

Trong bước này, bạn sẽ tạo một S3 Bucket để sử dụng cho việc lưu trữ dữ liệu trong bài lab này.

1. Truy cập [AWS S3 Console](https://ap-southeast-1.console.aws.amazon.com/s3).
2. Ở thanh điều hướng bên trái, chọn **General purpose buckets**.
3. Nhấn **Create bucket**.  

![buckets3](images/2.prerequisite/009-createbucket.png)

4. Tại trang **Create bucket**:
   - **Bucket type**: chọn **General purpose**.  
   - **Bucket name**: nhập **blog-micro-data-archive**.  
   - **Object Ownership**: chọn **ACLs disabled**.

![buckets3](images/2.prerequisite/010-createbucket.png)

5. Ở mục **Block Public Access**, giữ nguyên mặc định (để tích vào ô **Block all public access**).

![buckets3](images/2.prerequisite/011-createbucket.png)

6. Ở mục **Bucket key**, chọn **Disable**.

7. Để bật tính năng khóa đối tượng (ngăn xóa hoặc chỉnh sửa trong khoảng thời gian nhất định):
   - Trong **Advanced settings**, tại phần **Object Lock**, chọn **Enable** và tích ô xác nhận.
8. Click **Create bucket**

![buckets3](images/2.prerequisite/012-createbucket.png)
+++
title = "Dọn dẹp tài nguyên  "
date = 2025
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này.

#### Xóa EC2 instance

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
  + Click **Instances**.
  + Click **Instance state**.
  + Click **Terminate instance**, sau đó click **Terminate** để xác nhận.

![Clean](images/6.clean/001-cleanEC2.png)
![Clean](images/6.clean/002-cleanEC2.png)


#### Xóa S3 bucket

1. Truy cập [BUCKET](https://ap-southeast-1.console.aws.amazon.com/s3/home).
    + Click chọn Bucket
    + Click **Delete**
![Clean](images/6.clean/001-cleanS3.png)
- Vì các object vẫn còn tồn tại, bắt buộc phải xóa tất cả object có trong bucket trước khi xóa bucket.
![Clean](images/6.clean/002-cleanS3.png)
2. Tiếp theo:
    + Nhập `permanently delete` vào ô xác nhận.
    + Click **Empty**
![Clean](images/6.clean/003-cleanS3.png)
![Clean](images/6.clean/004-cleanS3.png)
3. Tiếp tục:
    + Nhập `blog-micro-data-archive` vào ô xác nhận.
    + Click **Delete bucket**
![Clean](images/6.clean/005-cleanS3.png)
![Clean](images/6.clean/006-cleanS3.png)



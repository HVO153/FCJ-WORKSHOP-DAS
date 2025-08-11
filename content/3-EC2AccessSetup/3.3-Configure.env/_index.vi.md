---
title : "Cấu hình file .env "
date :  "2024-06-08" 
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---


#### Cấu hình file .env

1. Mở project đã tải trước đó bằng Visual Studio Code
    + Vào thư mục **services**, tại đây ta thấy có 3 services: **user, author, blog**.
    + Tạo thêm file `.env` cho mỗi một service.


![env](images/3.InstanceSetup/012-env.png)

2. Dựa vào các hình ảnh bên dưới, bạn tự tạo và thêm lại các api vào các file **.env**
   
![env](images/3.InstanceSetup/env-user.png)

Ở 2 file **.env** của service author và blog, hãy thay **Rabbimq_Host** bằng **Public IPv4 address**.

![env](images/3.InstanceSetup/env-author.png)

File **.env** của **blog service** thay USER_SERVICE=`http://localhost:5000`.
![env](images/3.InstanceSetup/env-blog.png)


{{% notice note %}}
Vậy chúng ta đã xong phần thiết lập truy cập cho EC2, sang phần tiếp theo là **Thiết lập Lifecycle Policy cho Bucket S3**.
{{% /notice %}}

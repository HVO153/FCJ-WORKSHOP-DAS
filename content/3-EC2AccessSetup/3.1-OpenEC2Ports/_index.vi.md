---
title : "Mở cổng EC2 "
date :  "2024-06-08" 
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---


#### Mở các cổng EC2

1. Truy cập trang[EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home).
   + Click **Instances**.
   + Chọn instance **blogmicroservice**.

![portec2](/images/3.InstanceSetup/001-ports.png)

2. Chọn Tab **Security**.
   + Click vào đường dẫn bên dưới **Security groups**.

![portec2](/images/3.InstanceSetup/002-ports.png)
![portec2](/images/3.InstanceSetup/003-ports.png)

3. Tiếp theo:
   + Tại mục **Inbound rules** click vào **Edit inbound rules**.
   + Click **Add rule**, đặt cho **Port range** là `5672` và chọn **Anywhere-IPv4** ở  **Source**.
   + Tương tự với **Port range** `15672`.
   + Click **Save rules** để lưu thay đổi.
![portec2](/images/3.InstanceSetup/004-ports.png)

---
title : "Chuẩn bị VPC và EC2"
date :  "2024-06-08" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

{{% notice info %}}
Trong bước này, bạn cần tạo một VPC mới và một subnet mới.Sau đó tạo 1 EC2 Instance Ubuntu nằm trong subnet đó của VPC đó.
{{% /notice %}}

Tổng quan kiến trúc sau khi các bạn hoàn tất bước này sẽ như sau:

![VPC](images/arc-01.png)

Để tìm hiểu cách tạo các EC2 instance và VPC với  subnet các bạn có thể tham khảo bài lab :
  - [Giới thiệu về Amazon EC2](https://000004.awsstudygroup.com/vi/)
  - [Làm việc với Amazon VPC](https://000003.awsstudygroup.com/vi/) 


### Nội dung
  - [Tạo VPC](2.1.1-createvpc/)
  - [Tạo Subnet](2.1.2-createsubnet/)
  - [Tạo EC2 Ubuntu](2.1.3-createec2/)


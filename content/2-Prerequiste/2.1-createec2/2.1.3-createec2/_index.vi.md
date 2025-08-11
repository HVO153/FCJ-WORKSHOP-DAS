---
title : "Tạo EC2 Ubuntu"
date :  "2024-06-08" 
weight : 3 
chapter : false
pre : " <b> 2.1.3 </b> "
---


1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
   + Click **Instances**.
   + Click **Launch instances**.

![EC2](images/2.prerequisite/006-createec2.png)

2. Tại trang giao diện **Launch an instance**
   + Tại mục **Name** gõ **blogmicroservice**.
   + Tại mục **Application and OS Images** phần **Quick Start** chọn **Ubuntu**.
   + Tại mục **AMI** chọn **Ubuntu Server 24.04 LTS, SSD Volume Type**(Freetier).
  
![EC2](images/2.prerequisite/007-createec2.png)

3. Tiếp theo thực hiện 
   + Tại mục **Instance type** chọn **t2.micro**.
   + Tại mục **Key pair name** chọn **Create new key pair** và **(type:RSA,format: .pem)** nếu chưa có.
   + Tại mục **VPC-required** chọn VPC đã tạo trước đó.
  
![EC2](images/2.prerequisite/008-createec2.png)

4. Tiếp theo thực hiện
   + Tại mục **Auto-assign publicIP** chọn **Enable**.
   + Tại mục **Firewall** chọn **Create security group**.
   + Click **Launch instance** để tạo.
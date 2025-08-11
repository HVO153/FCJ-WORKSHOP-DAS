---
title : "Thiết lập Docker & RabbitMQ "
date :  "2024-06-08" 
weight : 2 
chapter : false
pre : " <b> 3.2 </b> "
---


#### Thiết lập Docker & RabbitMQ

1. Truy cập trang [EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home).
   + Click **Instances**.
   + Click chọn instance **blogmicroservice**.
   + Click **Connect**.

![package](images/3.InstanceSetup/005-package.png)

2. Tại trang **Connect to instance**
    + Chọn Tab **EC2 Instance Connect**.
    + Click **Connect**.

![package](images/3.InstanceSetup/006-package.png)

![package](images/3.InstanceSetup/007-package.png)

3. Tiếp theo, bạn copy từng lệnh và paste lên trên đây: 

```bash
sudo apt-get update -y

sudo apt-get install docker.io -y

sudo systemctl enable docker
sudo systemctl start docker

sudo usermod -aG docker $USER
newgrp docker

docker run -d --hostname rabbitmq-host \
--name rabbitmq-container \
-e RABBITMQ_DEFAULT_USER=admin \
-e RABBITMQ_DEFAULT_PASS=admin123 \
-p 5672:5672 \
-p 15672:15672 \
rabbitmq:3-management
```
Hiển thị các container:`docker ps -a`

Nếu container đã tồn tại nhưng bị dừng, bạn chỉ cần khởi động lại:`docker start rabbitmq-container`

![package](images/3.InstanceSetup/008-package.png)

4. Quay lại trang [EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Instances:)
    + Click chọn instance **blogmicroservice**.
    + Copy **Public IPv4 address** bên dưới.
    + Mở tab mới trên trình duyệt paste và thêm vào sau `:15672`.
    + Nhập **Username** : `admin`, **Password** : `admin123`.
    + Click **Login**.

![package](images/3.InstanceSetup/009-package.png)
![package](images/3.InstanceSetup/010-package.png)
![package](images/3.InstanceSetup/011-package.png)
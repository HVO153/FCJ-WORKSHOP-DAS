---
title: "Setup Docker & RabbitMQ"
date: "2024-06-08"
weight: 2
chapter: false
pre: " <b> 3.2 </b> "
---

#### Setup Docker & RabbitMQ

1. Access the page [EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home).  
   + Click **Instances**.  
   + Select the instance named **blogmicroservice**.  
   + Click **Connect**.

![package](/images/3.InstanceSetup/005-package.png)

2. On the **Connect to instance** page:  
   + Select the **EC2 Instance Connect** tab.  
   + Click **Connect**.

![package](/images/3.InstanceSetup/006-package.png)

![package](/images/3.InstanceSetup/007-package.png)

3. Next, copy and paste each command below into the terminal:

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
To list all containers, run:  
`docker ps -a`

If the container already exists but is stopped, you can restart it by running:  
`docker start rabbitmq-container`

![package](/images/3.InstanceSetup/008-package.png)

1. Return [EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/homeregion=ap-southeast-1#Instances:)  
   + Select the **blogmicroservice** instance.  
   + Copy the **Public IPv4 address** shown below.  
   + Open a new browser tab, paste the IP address, and append `:15672`.  
   + Enter **Username**: `admin`, **Password**: `admin123`.  
   + Click **Login**.

![package](/images/3.InstanceSetup/009-package.png)  
![package](/images/3.InstanceSetup/010-package.png)  
![package](/images/3.InstanceSetup/011-package.png)

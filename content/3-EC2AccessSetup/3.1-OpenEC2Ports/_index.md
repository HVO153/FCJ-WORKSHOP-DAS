---
title: "Open EC2 Ports"
date: "2024-06-08"
weight: 1
chapter: false
pre: " <b> 3.1 </b> "
---

#### Open EC2 Ports

1. Access the page[EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home).  
   + Click **Instances**.  
   + Select the instance named **blogmicroservice**.

![portec2](/images/3.InstanceSetup/001-ports.png)

2. Select the **Security** tab.  
   + Click the link under **Security groups**.

![portec2](/images/3.InstanceSetup/002-ports.png)  
![portec2](/images/3.InstanceSetup/003-ports.png)

3. Next:  
   + Under **Inbound rules**, click **Edit inbound rules**.  
   + Click **Add rule**, set the **Port range** to `5672`, and select **Anywhere - IPv4** for the **Source**.  
   + Repeat for the **Port range** `15672`.  
   + Click **Save rules** to apply the changes.

![portec2](/images/3.InstanceSetup/004-ports.png)

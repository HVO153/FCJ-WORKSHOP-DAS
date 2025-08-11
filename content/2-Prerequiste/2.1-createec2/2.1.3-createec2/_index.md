---
title : "Create EC2 Ubuntu"
date :  "2024-06-08" 
weight : 3 
chapter : false
pre : " <b> 2.1.3 </b> "
---

1. Go to the [EC2 Management Console](https://console.aws.amazon.com/ec2/v2/home)  
   + Click **Instances**.  
   + Click **Launch instances**.  

![EC2](/images/2.prerequisite/006-createec2.png)

2. On the **Launch an instance** page:  
   + In the **Name** field, enter **blogmicroservice**.  
   + In the **Application and OS Images** section under **Quick Start**, select **Ubuntu**.  
   + In the **AMI** field, choose **Ubuntu Server 24.04 LTS, SSD Volume Type** (Free Tier).  

![EC2](/images/2.prerequisite/007-createec2.png)

3. Next:  
   + In the **Instance type** field, select **t2.micro**.  
   + In the **Key pair name** field, choose **Create new key pair** and set **(type: RSA, format: .pem)** if you do not already have one.  
   + In the **VPC-required** field, select the VPC created earlier.  

![EC2](/images/2.prerequisite/008-createec2.png)

4. Continue:  
   + In the **Auto-assign public IP** field, select **Enable**.  
   + In the **Firewall** section, select **Create security group**.  
   + Click **Launch instance** to create.  

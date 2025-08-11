---
title: "Configure .env Files"
date: "2024-06-08"
weight: 3
chapter: false
pre: " <b> 3.3 </b> "
---

#### Configure .env Files

1. Open the previously downloaded project in **Visual Studio Code**.  
    + Go to the **services** directory. Here, you will see three services: **user**, **author**, and **blog**.
    + Create a new `.env` file for each service.

![env](/images/3.InstanceSetup/012-env.png)

2. Based on the images below, create and add the required API configurations into the `.env` files.

![env](/images/3.InstanceSetup/env-user.png)

In the `.env` files for **author** and **blog** services, replace **Rabbimq_Host** with **Public IPv4 address**.

![env](/images/3.InstanceSetup/env-author.png)

In the `.env` file for the **blog** service, replace USER_SERVICE=`http://localhost:5000`.

![env](/images/3.InstanceSetup/env-blog.png)

{{% notice note %}}
We have now completed the EC2 access configuration.  
Next, we will set up the **Lifecycle Policy for the S3 Bucket**.
{{% /notice %}}

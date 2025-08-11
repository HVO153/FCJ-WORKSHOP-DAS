---
title : "EC2 Access Setup"
date :  "2025-08-05"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

{{% notice info %}}
Once the EC2 instance is created, the next step is to configure the access ports and install the necessary packages.  
This ensures the server can run Docker and deploy the RabbitMQ container reliably, ready for subsequent tasks.
{{% /notice %}}

In this section, we will:

- Open the required ports to access EC2.
- Install packages to support running Docker.
- Add the container host path to the project’s .env file.

### Content
- [Open EC2 Ports](3.1-OpenEC2Ports/)
- [Set up Docker & RabbitMQ](3.2-SetupDocker&RabbitMQ/)
- [Configure .env](3.3-Configure.env/)
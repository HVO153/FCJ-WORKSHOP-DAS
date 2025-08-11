---
title : "Preparation Steps"
date :  "2025-08-05"
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

{{% notice info %}}
To complete this lab, you need to have an S3 Bucket, IAM access with S3 permissions, and an EC2 instance prepared in advance.
{{% /notice %}}

{{% notice note %}}
Since I have applied this topic to my own project, you may need to download the project as well to perform this lab.Download it [here](https://github.com/HVO153/Example-DASProject)
{{% /notice %}}


Before starting the implementation of the Data Archival Strategy, you should complete the following preparation steps:

- Create an EC2 Instance.
- Create an S3 Bucket to store long-term data.
- Create an IAM User or Role with full access to Amazon S3.

To learn how to create an S3 Bucket and configure permissions, refer to the following lab:

- [Working with Amazon S3](https://000005.awsstudygroup.com/vi/)

### Contents
  - [Prepare VPC and EC2 Instance](2.1-createec2/)
  - [Create S3 Bucket](2.2-creates3/)
  - [Create IAM User](2.3-createuseriam/)
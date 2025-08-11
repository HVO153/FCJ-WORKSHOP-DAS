---
title : "Create S3 Bucket"
date : "2024-06-08"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

### Create S3 Bucket

In this step, you will create an S3 Bucket to use for storing data in this lab.

1. Go to the [AWS S3 Console](https://ap-southeast-1.console.aws.amazon.com/s3).
2. In the left navigation pane, select **General purpose buckets**.
3. Click **Create bucket**.  

![buckets3](images/2.prerequisite/009-createbucket.png)

4. On the **Create bucket** page:
   - **Bucket type**: select **General purpose**.  
   - **Bucket name**: enter **blog-micro-data-archive**.  
   - **Object Ownership**: select **ACLs disabled**.

![buckets3](images/2.prerequisite/010-createbucket.png)

5. In the **Block Public Access** section, keep the default setting (leave **Block all public access** checked).

![buckets3](images/2.prerequisite/011-createbucket.png)

6. In the **Bucket key** section, select **Disable**.

7. To enable Object Lock (prevent deletion or modification for a specific period of time):
   - In **Advanced settings**, under **Object Lock**, select **Enable** and check the confirmation box.
8. Click **Create bucket**.

![buckets3](images/2.prerequisite/012-createbucket.png)

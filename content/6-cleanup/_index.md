+++
title = "Clean Up Resources"
date = 2025
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

We will follow these steps to delete the resources we created in this practice.

#### Delete EC2 Instance

1. Go to the [EC2 Management Console](https://console.aws.amazon.com/ec2/v2/home)  
   + Click **Instances**.  
   + Click **Instance state**.  
   + Click **Terminate instance**, then click **Terminate** to confirm.

![Clean](images/6.clean/001-cleanEC2.png)  
![Clean](images/6.clean/002-cleanEC2.png)  

#### Delete S3 Bucket

1. Go to [S3 Buckets](https://ap-southeast-1.console.aws.amazon.com/s3/home).  
   + Select the bucket.  
   + Click **Delete**.  

![Clean](images/6.clean/001-cleanS3.png)  

- Since objects still exist, you must delete all objects inside the bucket before deleting the bucket.  

![Clean](images/6.clean/002-cleanS3.png)  

2. Next:  
   + Enter `permanently delete` in the confirmation field.  
   + Click **Empty**.  

![Clean](images/6.clean/003-cleanS3.png)  
![Clean](images/6.clean/004-cleanS3.png)  

3. Continue:  
   + Enter `blog-micro-data-archive` in the confirmation field.  
   + Click **Delete bucket**.  

![Clean](images/6.clean/005-cleanS3.png)  
![Clean](images/6.clean/006-cleanS3.png)  

---
title: "Set Object Lock"
date: "2024-06-08"
weight: 2
chapter: false
pre: " <b> 4.2 </b> "
---

### Set Object Lock

To protect data from being deleted or modified, you need to set Object Lock for the bucket.

1. Go to [Bucket](https://ap-southeast-1.console.aws.amazon.com/s3/buckets).  
    + Inside the bucket, switch to the **Properties** tab.  
    + Find the **Object Lock** section and click **Edit**.  
    + Under **Default retention**, select **Enable**.  
    + For **Default retention mode**, choose **Compliance**.  
    + Set the object retention period.  
    + Click **Save changes** to apply.

![objlock](images/4.LifecyclePolicies/005-objlock.png)  
![objlock](images/4.LifecyclePolicies/006-objlock.png)  
![objlock](images/4.LifecyclePolicies/007-objlock.png)

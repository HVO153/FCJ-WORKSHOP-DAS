---
title: "Create Lifecycle Rule"
date: "2024-06-08"
weight: 1
chapter: false
pre: " <b> 4.1 </b> "
---

### Create Lifecycle Rule

In this step, you will create a lifecycle rule with two actions applied to the objects.

1. Go to [AWS BUCKET](https://ap-southeast-1.console.aws.amazon.com/s3/buckets/).
   + Select the bucket you created earlier: **blog-micro-data-archive**.
   + Switch to the **Management** tab.
   + Click **Create lifecycle rule** to start.

![lifecycle](/images/4.LifecyclePolicies/001-lifecycle.png)

2. Next:  
   + Enter **Lifecycle rule name**: `archive-to-glacier-and-delete`.
   + Set the **Rule scope** to **Apply to all objects in the bucket**.
   + Check the confirmation box **I acknowledge that this rule...**.
   + Check **Transition current versions of objects between storage classes**.
   + Check **Expire current versions of objects**.
   + Check the confirmation box **I acknowledge that this lifecycle...**.

![lifecycle](/images/4.LifecyclePolicies/002-lifecycle.png)

3. Then:  
   + Choose **Storage class transitions**: **Glacier Flexible Retrieval (formerly Glacier)**.
   + Set **Days after object creation** for transitioning storage class.
   + Set the expiration time for the object versions, creating a delete marker after the object is created.
   + Click **Create rule** to finish.

![lifecycle](/images/4.LifecyclePolicies/003-lifecycle.png)
![lifecycle](/images/4.LifecyclePolicies/004-lifecycle.png)

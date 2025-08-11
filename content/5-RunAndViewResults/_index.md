---
title: "Run and Results"
date: "2025-08-05"
weight: 5
chapter: false
pre: " <b> 5.</b> "
---

{{% notice info %}}
This section demonstrates running the project and reviewing the obtained results. It includes outcomes related to preventing deletion or modification through Object Lock, as well as automatic storage class transitions and object version expiration using Lifecycle Policies.
{{% /notice %}}

- You need to run `npm install` and `npm run build`, then `npm run dev` for each service when you first download it.
![conseque](/images/5.Consequence/001-runproject.png)
![conseque](/images/5.Consequence/002-runproject.png)
![conseque](/images/5.Consequence/003-runproject.png)

- Create a new post; the post's data will be sent to the S3 bucket. Then, check the bucket to verify whether it was stored successfully.
![conseque](/images/5.Consequence/004-runproject.png)
![conseque](/images/5.Consequence/005-runproject.png)
![conseque](/images/5.Consequence/006-runproject.png)

- Try deleting the data file in the bucket and see if the result matches the example below.
![conseque](/images/5.Consequence/007-deletefile.png)

- When you delete the data file, it is not actually removed. Enable **show version** to see that the file is marked with a delete marker, but the actual data still exists.  
  If you attempt to delete the original file, you will get the **Failed to delete objects** error. This confirms that the configured Object Lock is working correctly.
![conseque](/images/5.Consequence/008-deletefile.png)
![conseque](/images/5.Consequence/009-deletefile.png)

- Wait until the Object Lock retention period expires, then try deleting the file again.
![conseque](/images/5.Consequence/010-deletefile.png)
![conseque](/images/5.Consequence/011-deletefile.png)
![conseque](/images/5.Consequence/012-deletefile.png)

- After successful deletion, enable **show version** again; this time the file should be completely removed.
![conseque](/images/5.Consequence/013-deletefile.png)

- When the Object Lock expired on 2025-08-06 at 22:39:15, the file became eligible to transition to **Glacier Flexible Retrieval** according to the lifecycle rule. However, the actual transition occurred at around 21:50 on 2025-08-07 — roughly 22–23 hours later.
- This happens because AWS S3 does not perform lifecycle transitions instantly; they are processed according to internal scan schedules without a fixed execution time.
![conseque](/images/5.Consequence/014-glacier.png)

{{% notice note %}}
Therefore, in all cases, users should be aware that storage class transitions might be delayed compared to the expected time, even if the lifecycle rule is configured correctly.
{{% /notice %}}

{{% notice warning %}}
Note: The data file stored in the bucket must be larger than 218KB.  
If this condition is not met, the storage class transition will not occur.  
You need to ensure that when creating a post, the stored data size exceeds 218KB.
{{% /notice %}}

![conseque](/images/5.Consequence/016-restore.png)

- Once the object has transitioned to the **Glacier Flexible Retrieval** storage class, perform a **restore** to download and verify that the file's data integrity remains intact.
![conseque](/images/5.Consequence/017-restore.png)
![conseque](/images/5.Consequence/018-restore.png)
![conseque](/images/5.Consequence/019-restore.png)

- After a successful restore, you can either click **Open** to view it or **Download** to save it locally.
- Check the expiration time of the version, and revisit later to confirm if it has expired as expected.
![conseque](/images/5.Consequence/020-expiration.png)
![conseque](/images/5.Consequence/021-expiration.png)
![conseque](/images/5.Consequence/022-expiration.png)

- A sign that it is working correctly is when, upon visiting the **blog-micro-data-archive** bucket, you see no folders or files unless **show version** is enabled.

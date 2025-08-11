---
title: "Configuring Lifecycle Policies"
date: "2025-08-09"
weight: 4
chapter: false
pre: " <b> 4.</b> "
---
{{% notice info %}}
This is the main content of this Lab, with the goal of configuring **Lifecycle Policies** for an S3 Bucket.  
This allows stored data files to **automatically transition** to different storage classes, leveraging the specific advantages of each class (cost, performance, or long-term archival).  
In addition to automatic transitions, a Lifecycle Policy also supports various options such as deleting objects, expiring objects, or managing object versions based on a time period we define.
{{% /notice %}}

In this section, we will:
1. **Create a Lifecycle rule**:
   - Configure the **Transition current versions** action: Move the storage class of current object versions to another storage class.
   - Configure the **Expire current versions** action: Expire current versions and delete objects after a specified time.
2. **Set Object Lock**: Prevent deletion or overwrite of an object for a specific period of time.
3. **Add IAM access keys**: Create access keys for authentication when sending data from the project.

{{% notice note %}}
In addition to the two main actions above, a Lifecycle Policy also supports:  
\- **Transition noncurrent versions**: Move noncurrent (older) versions of an object to another storage class.  
\- **Permanently delete noncurrent versions**: Permanently delete noncurrent versions.  
\- **Delete expired object delete markers or incomplete multipart uploads**: Remove expired delete markers or unfinished multipart uploads.
{{% /notice %}}


### Content
- [Create Lifecycle Rule](4.1-CreateLifecycleRule/)
- [Set Object Lock](4.2-SetObjectLock/)
- [Create Access Key](4.3-CreateIamAccessKey/)
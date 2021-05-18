---
title: "Lab3 - Prepare the production target for application deployment"
chapter: true
weight: 6
---

## Setting Up an S3 Bucket to Host our target.

We will use an S3 bucket to host our deployed web site.
For that we have to create the following:

- Create IAM role that allows our runner to access S3.
- Attach our created role to our Gitlab Machine.
- Create an S3 bucket.
- Set the bucket for "Static Hosting" to allow public access to our site.


{{% notice warning %}}
We are going to create a publicly accessiable S3 bucket.
This bucket will be accessibale from the internet, and shoudnlt be used to store anything else, other than the sample site in this workshop.
{{% /notice  %}}
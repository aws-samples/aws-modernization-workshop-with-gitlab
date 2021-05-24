---
title: "Create and S3 Bucket and Setup Static Hosting"
chapter: true
weight: 64
---

## Create and S3 Bucket and Setup Static Hosting

To host our site we will leverage S3 Static Hosting capabilty.
First, we need to create an S3 bucket.

- In the AWS Console we select from the upper bar "Services" - > "S3"

- On The S3 page, select "Buckets" then "Create Bucket".
![s3cr-1](/images/s3cr_1.png)

- Give the bucket a unique name, then scroll down to the "Block Public Access settings" section.
![s3cr-2](/images/s3cr_2.png)

- In the "Block Public Access settings" section, Remove the check box next to "Block all public access", and add a check box at bottom to acknowldege public access.
![s3cr-3](/images/s3cr_3.png)

- Scroll down and click "Create Bucket".

### Next, we will setup our bucket for static hosting.

- From the bucket list, select our new bucket.

- Then click "Properties".
![s3cr-4](/images/s3cr_4.png)

- In the page that opend scroll all the way down, until you reach "Static website hosting", and click "Edit".
![s3cr-5](/images/s3cr_5.png)

- Select "Enable" int configiuration page, and write "index.html" under the index document.
![s3cr-6](/images/s3cr_6.png)

- Scroll down and select "Save Changes".

- Back in the properties page, under "Static website hosting", you will now see the link to our static website.
![s3cr-7](/images/s3cr_7.png)

### Finally, we will set the bucket policy to enable public access.

- On our bucket page click "Permissions".
![s3cr-8](/images/s3cr_8.png)

- Then scroll down to "Bucket Policy" and click "Edit".
![s3cr-9](/images/s3cr_9.png)

- Paste the following policy and change "BUCKET_NAME" to your S3 bucket name.
``` 
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::BUCKET_NAME/*"
        }
    ]
}
```
- Click "Save Changes" , and this will redirect you back the bucket page.
Where you should see an indicator that the bucket is now publicaly accessiable.
![s3cr-10](/images/s3cr_10.png)

### We are all set to deploy our website .

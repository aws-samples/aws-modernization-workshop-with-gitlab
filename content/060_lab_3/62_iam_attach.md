---
title: "Attach IAM Policy To Gitlab Runner"
chapter: true
weight: 62
---

## Attach IAM Policy To Gitlab Runner

For the Gitlab runner to use the role we just create, we must attach it to the EC2 Machine that runs our Runner.
In our case our Gitlab Server.

- In the AWS Console we select from the upper bar "Services" - > "EC2"
![iama-1](/images/iam_attach_1.png)

- Select our Gitlab machine, then click "Actions" -> "Security" -> "Modify IAM Role".
![iama-2](/images/iam_attach_2.png)

- From the dropdown in the page that opened select the we create in the previous step.
Then click "Save".
![iama-3](/images/iam_attach_3.png)


### Next, we will create an S3 that will store our website.
---
title: "Create an IAM Policy"
chapter: true
weight: 7
---

## Create an IAM Policy for the Gitlab Runner.

In order to be able to deploy our website to an S3 bucket we need to allow our runner to access S3.
We do that with an EC2 Instance policy that we attach to our Gitlab Instance.

- In the AWS Console we select from the upper bar "Services" - > "IAM"

- In the IAM Page we select "Roles" From the left side then "Create Role".
![iam-1](/images/iam_p1.png)

- In the Create Role Page, Select EC2 to create an instance profile, then click "Next"
![iam-2](/images/iam_p2.png)

- In the Attach Permissions Polices Page use the search bar to look for "AmazonS3FullAccess" Policy, Then Click "Next"
![iam-3](/images/iam_p3.png)

- On the Tags page, add any optional tags you might want, then click "Next"
![iam-4](/images/iam_p4.png)

- In the review page, enter a name for the policy and a description. then click "Create Role"
![iam-5](/images/iam_p5.png)

### Next, we will attach our new Role to the EC2 machine that runs Gitlab.
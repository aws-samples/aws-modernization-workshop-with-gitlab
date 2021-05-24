---
title: "Lab 1: Stand-up GitLab Ultimate"
chapter: true
weight: 4
---

## In This lab we will spin-up GitLab Ultimate AMI in AWS.

**:white_check_mark: Step-by-step Instructions**

- Open [GitLab Ultimate](https://aws.amazon.com/marketplace/pp/B07SJ817DX) in AWS Marketplace.
- Click on **Continue to Subscribe**
![aws-1](/images/aws-1.png)
- Sign in with your IAM user. (If you are asked to.)
![aws-2](/images/aws-2.png)
- Click on **Continue to Configuration**.
![aws-3](/images/aws-3.png)
- Leave the default value for **Delivery Method**, Select the latest version in **Software Version**, Select your **Region**, click **Continue to Launch**.
![aws-4](/images/aws-4.png)
- In Lunch this software page, scroll down.
![aws-5](/images/aws-5.png)
- Under **VPC Settings** Select the VPC that you want to deploy the gtilab instance on.
- Under **Subnet Settings** Select the ID of a Public Subnet that you want to deploy the gtilab instance on.
![aws-4](/images/aws-4-5.png)
- Under **Security Group Settings** click **Create New Based On Seller Settings** .
![aws-6](/images/aws-6.png)
- Name your security group, add a description, and Save it.
![aws-7](/images/aws-7.png)
- Select **Key Pair**. If you don't have key pair, create one. Leave other fields in this page with default values.  Click **Launch**.
![aws-8](/images/aws-8.png)
- You will get Congratulations message confirming you launched the machine successfully. In this message click on **EC2 Console** link.
![aws-9](/images/aws-9.png)
- Click on your instance ID link.
![aws-10](/images/aws-10.png)
{{% notice info %}}
The provisioning takes a few minutes. Please wait before you start the next step.
{{% /notice %}}
- Click Open address in order to open GitLab UI.
![aws-10_5](/images/aws-10_5.png)
- It takes a few minutes to start the server, you may see this error, this is ok, wait 1 minute and refresh the page.
![aws-11](/images/aws-11.png)
- You are now should be able to access GitLab login page. username is **root**, password is your **instance ID**, click **Sign in**.
![aws-13](/images/aws-13.png)
  :white_check_mark: Congratulations! you managed to start GitLab instance and sign in to it.
![aws-14](/images/aws-14.png)

---
title: "3. Create a VPC"
chapter: true
weight: 14
---

## Provision VPC

   [Click here to deploy using CloudFormation template](https://us-west-2.console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/create/template?stackName=ModernizationWorkshop-gitlab&templateURL=https://modernization-workshop-bucket.s3-us-west-2.amazonaws.com/cfn/master-stacks/vpc-only.yaml)

   - Create stack, click **Next**
   - Specify stack details, click **Next**
   - Configure stack options, click **Next**
   - Scroll to bottom section under **Capabilities** and check both boxes and click **Create stack**


This template deploys a VPC, with a pair of public and private subnets spread
across two Availability Zones. It deploys an internet gateway, with a default
route on the public subnets. It deploys a pair of NAT gateways (one in each AZ), and default routes for them in the private subnets.

This will take a couple of miuntes to deploy.

When the deployment is complete go to "Services" -> "VPC",
To see the list of VPC on the account.

Click on "Your VPCs" from the left side, this will take you to the list of VPC on this account.
![vpc-1](/images/vpc-1.png)
From the list select the VPC Named **Workshop**, and note the VPC-ID for use in the next step
![vpc-2](/images/vpc-2.png)
Next click on "Sunbets" on the left side.
![vpc-3](/images/vpc-3.png)
From the list, select a subnet that is called **Workshop Public Subnet (AZ2)**, and note the SUBNET-ID for use in the next step.
![vpc-4](/images/vpc-4.png)

Now lets continue to the next step.

{{% notice info %}}
For the purposes of this workshop we will deploy our Gitlab machine on a Public network with a Public IP.
This is not recomended for a production setup.
{{% /notice %}}

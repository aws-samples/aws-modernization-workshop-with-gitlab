---
title: "Cleanup"
chapter: true
draft: false
weight: 10
---

# Workshop Cleanup

We have created several resources in this workshop and we want to make sure that we remove them after we are done experimenting, to not incur additional charges.

### S3 Bucket Removal
- In our AWS Console, Click "Services" -> "S3".
- Select the bucket we created earlier, and click the "Delete" button on the upper right croner.
- Confirm the bucket deletion by entering the bucket name in the input field.
- Then click "Delete Bucket".
- Confirm that the bucket was delete by making sure its not on the bucket list.

### EC2 Machine Removal
- In our AWS Console, Click "Services" -> "EC2".
- Select "Instances" from the left-hand side, and select our Gitlab machine from the list.
- Click the "Instance State" button on the right-hand side, and choose "Terminate instance".
- Click "Terminate" in the dialog that opens, to confirm.

### Marketplace Subscription Removal
- In our AWS Console, Click "Services" -> "AWS Marketplace Subscriptions".
- Under the "Gitlab Ultimate" subscription, click the "Manage" button.
- Click the "Actions" button on the right-hand side and select "Cancel Subscription".
- In the dialog that comes up, check the checkbox, and click "Yes, cancel subscription".

### Cloudformation VPC Template Removal
- In our AWS Console, Click "Services" -> "Cloudformation".
- In the list of Stacks, select "ModernizationWorkshop-gitlab", and click the "Delete" button on the right corner.
- In the dialog that opend click "Delete Stack" to remove the Cloudformation stack we created.
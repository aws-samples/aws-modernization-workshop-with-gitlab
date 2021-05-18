---
title: "Summary"
chapter: true
weight: 9
---

# Summary

In this workshop we learned:

 main

## Cleanup

we have create several resources in this work shop and we want to make sure that we remove them after we are done experimenting,
So not incurr additional charges.

### S3 Bucket Removal
- In our AWS Console, Click "Services" -> "S3".
- Select the bucket we created earlier, and click the "Delete" button on the upper right croner.
- Confirm the bucket deletion by entering the bucket name in the input field.
- Then click "Delete Bucket".
- Confirm that the bucket was delete by making sure its not on the bucket list.

### EC2 Machine Removal
- In our AWS Console, Click "Services" -> "EC2".
- Select "Instances" from the left hand side, and select our Gitlab machine from the list.
- Click the "Instance State" button on the right hand side, and choose "Terminate instance".
- Click "Terminate" in the dialog that opens, to confirm.

### Marketplace Subscription Removal
- In our AWS Console, Click "Services" -> "AWS Marketplace Subscriptions".
- Under the "Gitlab Ultimate" subscription, click the "Manage" button.
- Click the "Actions" button on the right hand side and select "Cancel Subscription".
- In the dialog that comes up, check the check box, and click "Yes, cancel subscription".

=======
- How to stand-up **GitLab Ultimate** in **AWS** via the **marketplace**.
- How to install GitLab **Runner** and register it to our GitLab project.
- How to create a new project and import a repository to it.
- How to configure GitLab CI/CD via the **.gitlab-ci.yml** file.
- How to save **secrets** in GitLab **Variables** in the **CI/CD settings**.  
- How to use **GitLab DevOps platform** to **build**, **test** and **deploy** applications.
main

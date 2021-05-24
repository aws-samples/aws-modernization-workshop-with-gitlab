---
title: "LAB5 - Development flow: change code, build, test, and deploy"
chapter: true
weight: 8
---

# Development flow: change code, build, test, and deploy

Now that we have a project configured with CI/CD that build, test and deploy the app, we can make a change to the website, test, and deploy it

From the project overview page, open the Web IDE.
![yml-1](/images/yml-1.png)

From the left pane, open the file **index.js** under **/src/pages**
![code-1](/images/code-1.png)
Modify the code, replace the text **Now go build something great** with
`With GitLab you can iterate faster, innovate together: Our open DevOps platform is a single application for unparalleled collaboration, visibility, and development velocity.`

![code-2](/images/code-2.png)
Commit the change, click Commit.

 - Add a commit message.

 - Change the default commit option to Commit to master.

 - Click Commit.

Wait for the pipeline to complete.

:white_check_mark: Well done! You manages to run through a full development flow with GitLab CI/CD!

Check the website to see your change deployed.

---
title: "Configure the .gitlab-ci.yml file in the project"
chapter: true
weight: 2
---


# Configure the CI/CD in the project

In the root of the project you imported in **lab2** there is already **.gitlab-ci.yml** file that includes **build** and **test** **stages**, and **jobs** in each stage.

We will add one additional **stage** and **jobjobs** to this configuration file,  **deploy**:

  - **deploy**  will deploy the sample website to **surge**.

Open the Web IDE.
![yml-1](/images/yml-1.png)
On the left, open the .gitlab-ci.yml file.
![yml-2](/images/yml-2.png)
You will notice **stages** keyword, with **build** and **test** stages.
Add **deploy** stage to it.

Your stages now should look like this:

{{< highlight html >}}
stages:
  - build
  - test
  - deploy
{{< /highlight >}}

Scroll down, and create a deploy job in the deploy stage.

  - Job name: **deploy to s3**
  - stage: **deploy**
  - add the following scripts:
    - `curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"`
    - `unzip -q awscliv2.zip`
    - `./aws/install`
    - `aws s3 cp ./public s3://mytestwebsite211/ --recursive`

Your deploy job should look like this one:

{{< highlight html >}}
deploy to s3:
  stage: deploy
  script:
    - curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
    - unzip -q awscliv2.zip
    - ./aws/install 
    - aws s3 cp ./public s3://mytestwebsite211/ --recursive
{{< /highlight >}}

Commit the change, click Commit.
![commit-1](/images/commit-1.png)

 - Add a commit message.

 - Change the default commit option to Commit to master.

 - Click Commit.
![commit-2](/images/commit-2.png)

Wait a few seconds until you will see in the status bar, below the commit button, the pipeline ID, click on it in order to open the pipeline.
![commit-3](/images/commit-3.png)

This will open the Pipeline graph
![commit-4](/images/commit-4.png)
You can click on each job to check it log. wait until the **deploy to s3** job completes, when it has a green **V** icon.

Make sure all jobs passed successfully, and that pipeline status is **passed**.
![pipeline-5](/images/pipeline-5.png)
Open in the browser the domain of our S3 Bucket and you will be able to see the website.

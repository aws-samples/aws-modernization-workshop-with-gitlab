---
title: "Install and register Runner"
chapter: true
weight: 6
---

### :star:Lab Objectives

Runner machines are the build agents that run the CI/CD jobs. We will install GitLab Runner and Docker engine. We run all jobs inside the images, and therefore the runner machine requires Docker engine on the runner machine.

We will configure the Runner and register it to work with our GitLab project.

{{% notice note %}}
Running jobs inside container has several advantages:
Jobs are isolated which avoid compatibility issues, and they run in a secured environment. Once a job completes, the image is being destroyed and nothing is left on the runner machine.
Also, you don't need to install any build tool on the runner machine, all prerequisite tools available in the standard or custom Docker image.
For more information about running jobs in docker containers, visit https://docs.gitlab.com/ee/ci/docker/using_docker_images.html#run-your-cicd-jobs-in-docker-containers
{{% /notice  %}}



{{% notice warning %}}
It is not recommended best practice to install Runners on the same machine when the server installed for security and performance reasons, but only for the sake of simplicity, in this workshop we will install it on the same machine.
{{% /notice  %}}

{{% notice tip %}} GitLab Runner is open-source and written in Go. It can be run as a single binary; no language-specific requirements are needed. You can install GitLab Runner on several different supported operating systems. Other operating systems may also work, as long as you can compile a Go binary on them.
{{% /notice %}}


# Install Docker engine   
  - Go to your Instance summary, and click **Connect** in order to open the console.
  ![runner-1](/images/runner-1.png)
  - Click Connect again.
  ![runner-2](/images/runner-2.png)
  - Install Container by running this command `curl -fsSL https://get.docker.com -o get-docker.sh
   sudo sh get-docker.sh`

# Setup Runners


  - Download the binaries for Linux x86 `sudo curl -L --output /usr/local/bin/gitlab-runner "https://gitlab-runner-downloads.s3.amazonaws.com/latest/binaries/gitlab-runner-linux-386"`
  - Give it permissions to execute: `sudo chmod +x /usr/local/bin/gitlab-runner`
  - Create a GitLab CI user: `sudo useradd --comment 'GitLab Runner' --create-home gitlab-runner --shell /bin/bash`
  - Install and run as service: `sudo gitlab-runner install --user=gitlab-runner --working-directory=/home/gitlab-runner
sudo gitlab-runner start`

# Register the Runner

  - Run this command: `sudo gitlab-runner register`.
  - You will be prompt to enter URL.
  - Open your GitLab instance, under CI/CD settings:
    - Click Settings->CI/CD.
      ![runner-2](/images/runner-3.png)
    - Expand **Runners**.
      ![runner-4](/images/runner-4.png)
    - Copy the URL to the clipboard under specific runner.
    ![runner-5](/images/runner-5.png)
  - Pater the URL in the console.
  - Enter.
  - You will be prompt to enter registration token, copy it from the Runner settings.
![runner-5](/images/runner-6.png)
  - Paste it in the console.
  - Enter Description for the runner: type **GitLab workshop**.
  - Add a tag to this runner, for example type **Linux**
  - Enter executor, type **docker**.
  - Enter the default Docker image, type **ruby:2.6**.
  - You will get a message starting with **Runner registered successfully. Feel free to start it...**
  - Refresh the Runner settings page in GitLab and you will see your runner under **Available specific runners**.
  - Click edit.
  ![runner-7.png](/images/runner-7.png)
  - Check the **Indicates whether this runner can pick jobs without tags** option, and click **Save changes**.
  ![runner-7.png](/images/runner-8.png)


  :white_check_mark:**Well done!! you installed and registered successfully GitLab Runner.**

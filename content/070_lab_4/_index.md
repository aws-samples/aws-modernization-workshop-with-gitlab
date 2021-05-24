---
title: "Lab 4: CI/CD configuration"
chapter: true
weight: 7
---

## CI/CD configuration

In GitLab, the CI/CD configuration is made via code. In order to enable CI/CD, you need to create [.gitlab-ci.yml](https://docs.gitlab.com/ee/ci/yaml/gitlab_ci_yaml.html) file in [YAML](https://en.wikipedia.org/wiki/YAML) format, and save it in the root of your repository.


In this file, you define:

- The structure and order of jobs that the runner should execute.
- The decisions the runner should make when specific conditions are encountered.

For example, you might want to run a suite of tests when you commit to any branch except the default branch. When you commit to the default branch, you want to run the same suite, but also publish your application.

All of this is defined in the **.gitlab-ci.yml** file.

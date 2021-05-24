---
title: "CI/CD"
chapter: true
weight: 12
---

# Continuous Integration (CI)

<iframe width="560" height="315" src="https://www.youtube.com/embed/ljth1Q5oJoo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

The Continuous Integration (CI) use case is a staple of modern software development in the digital age. It's unlikely that you hear the word "DevOps" without a reference to "Continuous Integration and Continuous Delivery" (CI/CD) soon after. In the most basic sense, the CI part of the equation enables development teams to automate building and testing their code.

When practicing CI, teams collaborate on projects by using a shared repository to store, modify and track frequent changes to their codebase. Developers check in, or integrate, their code into the repository multiple times a day and rely on automated tests to run in the background. These automated tests verify the changes by checking for potential bugs and security vulnerabilities, as well as performance and code quality degradations. Running tests as early in the software development lifecycle as possible is advantageous in order to detect problems before they intensify.

CI makes software development easier, faster, and less risky for developers. By automating builds and tests, developers can make smaller changes and commit them with confidence. They get earlier feedback on their code in order to iterate and improve it quickly increasing the overall pace of innovation. Studies done by DevOps Research and Assessment (DORA) have shown that [robust DevOps practices lead to improved business outcomes](https://cloud.google.com/devops/state-of-devops/). All of these "DORA 4" metrics can be improved by using CI:

- **Lead time:** Early feedback and build/test automation help decrease the time it takes to go from code committed to code successfully running in production.

- **Deployment frequency:** Automated build and test is a pre-requisite to automated deploy.

- **Time to restore service:** Automated pipelines enable fixes to be deployed to production faster reducing Mean Time to Resolution (MTTR)

- **Change failure rate:** Early automated testing greatly reduced the number of defects that make their way out to production.
  GitLab CI/CD comes built-in to GitLab's complete DevOps platform delivered as a single application. There's no need to cobble together multiple tools and users get a seamless experience out-of-the-box.

# Continuous Delivery

“Deployment is manual”

“Functional tests are manual”

“Time consuming or lack of rollback on performance degradation or production errors”

“Hard to maintain environment configurations and hard to operate”

“No consistency in deployment process”

“Manual / hard coded configurations”

“No standardized software artifact”

“No release management in place”

“Too dependent on other teams to get any release done”

If these are the typical problems you face, Continuous Delivery is for you.

Continuous Delivery is the next logical step after continuous integration and it streamlines and automates the application release process to make software delivery repeatable and on demand - from provisioning the infrastructure environment to deploying the tested application software to test/staging or production environments. Organizations practicing continuous delivery are able to plan their release processes and schedules, automate infrastructure and application deployments, manage deployed infrastructure and application resources resources, and analyze metrics to optimise the software delivery process.

## Why Continuous Delivery?

**Consistent & repeatable release process** - lesser manual processes imply the release process is less error prone and hence can be repeatable for every minimal change to the code

**Faster time to market** - automation of environment provisioning, software deployment and rapid feedback helps teams to iterate faster and rollback when necessary

**Lower risk releases** - by using progressive delivery practices such as advanced deployments: incremental / blue green / canary deployments, review apps, feature flags and a deployment performance feedback loop, organizations are able to validate their software before widespread deployment

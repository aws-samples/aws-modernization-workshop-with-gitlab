---
title: "GitOps"
chapter: true
draft: false
weight: 14
---
# GitOps

## The need for GitOps

Modern applications are developed with rapid iteration and run at highly dynamic scale. In an organization with a mature DevOps culture code can be deployed to production hundreds of times per day. Applications can then run under highly dynamic loads from a few users to millions. Modern infrastructure needs to be elastic. Capacity that can be dynamically provisioned and de-provisioned is able to keep pace with load maintaining optimal performance and minimal cost. With the demands made on today's infrastructure it's becoming increasingly crucial manage infrastructure automation with a robust and cohesive methodology.

## What is GitOps?

GitOps == IaC + MRs + CI/CD

GitOps is an operational framework that takes DevOps best practices used for application development such as version control, collaboration, compliance, and CI/CD, and applies them to infrastructure automation.

<iframe width="560" height="315" src="https://www.youtube.com/embed/JtZfnrwOOAw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

GitOps involves managing your IT infrastructure using practices well-known in software development such as version control, code review, and CI/CD pipelines. For example, infrastructure teams that practice GitOps use configuration files stored as code. Similar to how application source code generates the same application binaries every time it's built, GitOps configuration generates the same infrastructure environment every time it is deployed.

- **IaC** - GitOps uses a Git repository as the single source of truth for infrastructure definition. Infrastructure as Code (IaC) is the practice of keeping all infrastructure configuration stored as code. The actual desired state may or may not be not stored as code (e.g., number of replicas, pods).

- **MRs** - GitOps uses Merge Requests (MRs) as the change mechanism for all infrastructure updates. The MR is where teams can collaborate via reviews and comments and where formal approvals take place. Merge commits to your master(or trunk) branch serve as a change log for auditing and troubleshooting.

- **CI/CD** - GitOps automates infrastructure updates using a Git workflow with Continuous Integration and Continuous Delivery (CI/CD). When new code is merged, the CI/CD pipeline enacts the change in the environment. Any configuration drift, such as manual changes or errors, is overwritten by GitOps automation so the environment converges on the desired state defined in Git. GitLab uses CI/CD pipelines to manage and implement GitOps automation, but other forms of automation such as definitions operators could be used as well.

As with any emerging technology term, "GitOps" isn't strictly defined the same way by everyone across the industry. GitOps emerged in the cloud native community and some definitions restrict GitOps to say "Kubernetes is required to be doing GitOps." GitLab takes a broader approach. We've seen GitLab users and customers applying GitOps principals to all types of infrastructure automation including VMs and containers, as well as Kubernetes clusters.

While many tools and methodologies promise faster deployment and seamless management between code and infrastructure, GitOps differs by focusing on a developer-centric experience. Infrastructure management through GitOps happens in the same version control system as the application development, enabling teams to collaborate more in a central location while benefiting from all the built-in features of Git.

GitOps is a prescriptive workflow for using Infrastructure as Code. GitOps with GitLab helps you manage physical, virtual and cloud native infrastructures (including Kubernetes and serverless technologies) using tight integration with industry-leading infrastructure automation tools like Terraform, AWS Cloud Formation, Ansible, Chef, Puppet, and the like.

## Benefits of GitOps

Distribution of work - Enable more engineers to collaborate on infrastructure changes. Since every change will go through the same change/merge request/review/approval/merge process, this enables senior engineers to focus on other areas beyond the critical infrastructure management while still maintaining the ability to review and contribute as needed.

- **Improved access control** There's no need to give credentials to all infrastructure components since changes are automated only by your CI/CD needs access.

- **Faster time to market** - execution via code is faster than manual point and click, test cases can be automated and hence repeatable in a consistent manner to deliver stable environments rapidly, at scale

- **Less risk** The shift-left approach to infrastructure as Code helps to identify and resolve issues before changes are rolled out to production preempting unexpected downtime and providing higher environment stability and reliability and better user experience.

- **More compliant** All changes to infrastructure are tracked, leaving traceability for audit and ability to rollback to a previous desired state with ease.

- **Reduce costs** - automation of infrastructure definition and testing eliminates manual tasks and rework improving productivity, reduced downtimes due to built in revert/rollback capability

- **Less error prone** - infrastructure definition is codified, hence repeatable and less prone to human error

## Push vs Pull GitOps (Agentless vs Agent Based GitOps)

As with any emerging technologies, there are different approaches to GitOps, each with their own pros and cons.

**Push or Agentless GitOps** In this approach, your CI/CD tool pushes the changes to your environment. This approach is consistent with the approach used for application deployment. Pro

Ease of use. Well-known CI/CD - build, test, & deploy all use the same tech
Deployment targets not limited to cloud native / Kubernetes only - can deploy to physical, virtual container - whether onpremise or cloud etc. Con
Need to open your firewall to your cluster and grant admin access to external CI/CD

**Pull or Agent Bsed GitOps** In this approach, an agent is installed in your cluster to pull changes whenever there is a drift from the desired configuration. Pro

Secure infrastructure - no need to open your firewall or grant admin access externally Con
Agent needs to be installed in every cluster
Limited to k8s-only
Uses different technology than application CI/CD

:white_check_mark: Check out the market viewpoint on the [GitOps use case](https://about.gitlab.com/handbook/marketing/strategic-marketing/usecase-gtm/gitops/) for a more in-depth explanation.

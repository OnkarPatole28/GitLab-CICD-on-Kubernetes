- GitLab is a web-based DevOps platform built around Git that enables teams to manage the entire software development lifecycle from a single application. 
- It provides features such as source code management, issue tracking, CI/CD pipelines, and package and container registries. 
- GitLab acts as a centralized hub for hosting repositories and extends Git’s capabilities by integrating planning, automation, security, and deployment workflows.



✅ GitLab Architecture

GitLab Server: stores repositories, pipelines, and job definitions.

GitLab Runner: 
  - Executes CI/CD jobs.
  - Runners are external machines or virtual machines that are responsible for running your pipeline jobs upon       triggering. They register with the GitLab server to receive and process job execution.

  2 types of Runners:
  ✔ SaaS / Shared Runners : Hosted and managed by GitLab. SaaS runners are pre-provisioned and reused.
  ✔ Self-managed Runners:  Installed and managed by you. Can run on VM, cloud, Kubernetes, etc.


Executor: 
-  Defines how and where the job runs on runner machines:
 - Docker
 - Shell
 - Virtual machine
 - SSH


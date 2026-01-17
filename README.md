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


 

 Tag:
 - The tags keyword is used in a GitLab CI/CD pipeline to select which GitLab Runner should execute a job.
 - GitLab selects a runner based on matching tags. If no tags are specified, GitLab uses shared runners.
 - When a GitLab CI job has multiple tags, GitLab will look for a single runner that has all of the specified tags. If no runner has all tags → job stays pending. In below example Gitlab will try to find a runner which has both the tags (docker and linux).
 tags:
  - docker
  - linux



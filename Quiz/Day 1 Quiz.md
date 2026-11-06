## Day 1 --- DevOps Fundamentals & Git

1.  Define DevOps in your own words.
2.  What problems can occur when Development and Operations teams work
    in silos?
3.  List the major stages of the DevOps lifecycle in order.
4.  Explain the difference between Continuous Integration (CI) and
    Continuous Delivery/Deployment (CD).
5.  What is Infrastructure as Code (IaC), and why is it useful?
6.  Name four tools commonly used in a DevOps workflow and state what
    each does.
7.  What is a Git repository?
8.  Explain the purpose of `git status`, `git add`, and `git commit`.
9.  Write commands to:
    -   Configure your Git username and email.
    -   Initialize a repository in the current directory.
    -   Stage all changes.
    -   Commit staged changes with the message `Initial commit`.
10. What is the difference between `git log` and `git status`?

------------------------------------------------------------------------

## Answer Key

1.  DevOps combines culture, practices, and tools to improve
    collaboration and automate reliable software delivery.
2.  Slow handoffs, blame, inconsistent environments, delayed releases,
    and unclear ownership.
3.  Plan → Code → Build → Test → Release → Deploy → Operate → Monitor
    (teams may represent the lifecycle differently).
4.  CI integrates and tests code frequently; CD automates delivery
    and/or deployment after validation.
5.  IaC defines infrastructure through version-controlled configuration,
    making it repeatable and reviewable.
6.  Examples: Git (version control), Docker (containers), Jenkins
    (automation/CI), Terraform (IaC), AWS (cloud), Prometheus
    (monitoring).
7.  A repository stores project files and their version history.
8.  `status` shows working-tree/staging state; `add` stages changes;
    `commit` records staged changes.
9.  `git config --global user.name "Your Name"`;
    `git config --global user.email "you@example.com"`; `git init`;
    `git add .`; `git commit -m "Initial commit"`.
10. `git status` shows current changes; `git log` shows commit history.
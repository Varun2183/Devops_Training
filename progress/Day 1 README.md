# DevOps Training

## Day 1 – DevOps Fundamentals & Environment Setup

### Learning Objectives
- Understand DevOps fundamentals.
- Understand the DevOps lifecycle.
- Learn CI, CD, automation, IaC, and monitoring.
- Understand essential DevOps tools.
- Set up Ubuntu using WSL2 on Windows 11.
- Configure Git and create the first repository.

### 1. DevOps Fundamentals

DevOps = Development + Operations.

DevOps is a culture and set of practices that improves collaboration between development and operations teams through automation, continuous integration, continuous delivery, and monitoring.

#### Benefits
- Faster software delivery
- Improved collaboration
- Reliable deployments
- Reduced manual work
- Faster feedback
- Better application stability

### 2. DevOps Lifecycle
1. Plan
2. Code
3. Build
4. Test
5. Release
6. Deploy
7. Operate
8. Monitor

### 3. Important Concepts

- **CI:** Automatically builds and tests code changes.
- **Continuous Delivery:** Keeps software ready for release, generally with production approval.
- **Continuous Deployment:** Automatically deploys qualifying changes to production.
- **Automation:** Performs repetitive tasks using scripts and tools.
- **Infrastructure as Code:** Defines infrastructure using configuration files.
- **Monitoring:** Tracks application and infrastructure health.
- **Version Control:** Tracks and manages code changes.

### 4. DevOps Tools Overview

| Tool | Purpose |
|---|---|
| Git | Version control |
| GitHub | Code hosting and collaboration |
| Linux | Operating system |
| Docker | Containerization |
| Kubernetes | Container orchestration |
| Jenkins | CI/CD automation |
| Terraform | Infrastructure as Code |
| Ansible | Configuration management |
| AWS | Cloud infrastructure |
| Prometheus | Monitoring |
| Grafana | Metrics visualization |

### 5. Windows 11 Environment Setup

Install WSL2:

```powershell
wsl --install
```

Verify:

```powershell
wsl --list --verbose
```

Update Ubuntu:

```bash
sudo apt update
sudo apt upgrade -y
```

Install tools:

```bash
sudo apt install git curl wget vim tree -y
```

### 6. Linux Commands Learned

| Command | Purpose |
|---|---|
| pwd | Current directory |
| ls | List files |
| ls -la | List files including hidden files |
| whoami | Current username |
| date | Current date and time |
| uname -a | System information |
| df -h | Disk usage |
| free -h | Memory usage |
| mkdir | Create directory |
| cd | Change directory |
| touch | Create file |
| echo | Print/write text |
| cat | Display file contents |
| sudo | Elevated privileges |
| apt | Package management |

### 7. Git Basics

Configure Git:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Create repository:

```bash
git init
git status
git add notes.txt
git commit -m "Day 1: DevOps learning notes"
git log --oneline
```

### 8. Practical Assignments
- Install WSL2 and Ubuntu.
- Update Ubuntu packages.
- Install Git and essential utilities.
- Create `~/devops-training/day01`.
- Create `notes.txt`.
- Configure Git identity.
- Initialize a Git repository.
- Create the first Git commit.

### 9. Interview Topics
- What is DevOps?
- Why is DevOps needed?
- Explain the DevOps lifecycle.
- Explain CI, CD, and automation.
- What is Infrastructure as Code?
- What is version control?
- Explain the purpose of Git, Docker, Kubernetes, Jenkins, Terraform, and AWS.

### 10. Day 1 Completion Checklist
- [ ] Understand DevOps fundamentals.
- [ ] Explain the DevOps lifecycle.
- [ ] Understand CI/CD.
- [ ] Understand automation and IaC.
- [ ] Install Ubuntu through WSL2.
- [ ] Practice Linux commands.
- [ ] Configure Git.
- [ ] Create first Git repository and commit.
- [ ] Complete Day 1 evaluation.

---


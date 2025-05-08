# Introduction

### Why we need Ansible?

Ansible is an agentless architecture which automates the task (configuration management) of system admins:

1. Making system up to date ✓
2. Package up to date ✓
3. Manage application dependencies ✓
4. Maintain and manage multiple servers efficiently ✓

Shell script might fail - Ansible solves that

Ex: For centos yum is default package manager but for ubuntu it is apt. Ansible solves these kinds of problem.

**Ansible Workflow:**
Ansible → YAML → Playbook _(Agentless automation)_

### Installation:

Before installing the ansible the pip needs to be installed.

```bash
sudo apt update
sudo apt install python3-pip
pip install ansible
```

### **Terminology**

- **Control Node:** The machine (typically your local or a VM) where Ansible is installed.
- **Managed Nodes:** Remote machines managed by the control node using SSH.

![Image](https://github.com/user-attachments/assets/35943e4f-a1a8-477a-ba14-0c5f514d44ce)

### All use-cases of Ansible (automation platform):

1. Provisioning ec2, s3 bucket, vm etc
2. Configuration Management
3. Deployment (CI/CD) ex: deploy app on multiple vm/clusters/kubernetes
4. Network Automation (talking with network appliances ex: automating vlan)

> **Requirement:** Python must be installed on all managed nodes.

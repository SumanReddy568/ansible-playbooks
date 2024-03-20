# Ansible Playbooks Repository

Welcome to the Ansible Playbooks Repository! This repository contains a collection of Ansible playbooks for various tasks and purposes.

## Overview

Ansible is an open-source automation tool used for configuration management, application deployment, task automation, and orchestration. It simplifies complex tasks by allowing you to describe infrastructure configurations in simple YAML files, called playbooks, which are easy to read, write, and understand.

## Contents

### 1. Ad-hoc Commands

Ad-hoc commands are used for performing quick tasks on remote hosts without the need for writing a playbook. These commands are particularly useful for tasks like gathering information, installing packages, restarting services, etc.

Example:
```shell
ansible all -i inventory.ini -m command -a "uptime" 


Playbooks are Ansible's configuration, deployment, and orchestration language. They can describe a policy you want your remote systems to enforce or a set of steps in a general IT process. Each playbook is composed of one or more plays, and each play is a mapping between a set of hosts and tasks.

---
- name: Example Playbook
  hosts: all
  tasks:
    - name: Ensure NTP is installed and running
      yum:
        name: ntp
        state: present
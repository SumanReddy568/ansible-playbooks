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

### 2. Playbooks

Playbooks are Ansible's configuration, deployment, and orchestration language. They can describe a policy you want your remote systems to enforce or a set of steps in a general IT process. Each playbook is composed of one or more plays, and each play is a mapping between a set of hosts and tasks.

Example playbook structure:
```yaml
---
- name: Example Playbook
  hosts: all
  tasks:
    - name: Ensure NTP is installed and running
      yum:
        name: ntp
        state: present

### 3. Advanced Ansible Concepts

#### Roles

Roles are a way to organize and package related tasks, handlers, variables, and other files in a reusable and modular way. They allow you to break down complex playbooks into smaller, more manageable components.

#### Variables and Templating

Ansible allows you to use variables to make your playbooks more dynamic and reusable. You can define variables at various levels, including at the playbook, role, or inventory level, and use them in your tasks, templates, and other files using Jinja2 templating.

#### Conditionals and Loops

Ansible provides support for conditionals and loops, allowing you to control the flow of your playbooks and perform repetitive tasks based on certain conditions or iterate over lists of items.

#### Handlers

Handlers are tasks that are triggered by other tasks in your playbook, typically in response to changes in the system state. They are useful for tasks like restarting services or reloading configuration files after changes have been made.

#### Vault

Ansible Vault allows you to encrypt sensitive data, such as passwords or secret keys, within your playbooks and roles. This ensures that sensitive information is stored securely and can only be accessed by authorized users.
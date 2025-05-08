## **Playbook**

An Ansible playbook is a file containing a set of instructions to automate tasks on remote hosts using Ansible. It is written in YAML and is the core component of Ansible configuration management.

### **Play:**

A play is the core unit of Ansible execution, consisting of a list of tasks mapped to specific managed hosts.

### **Modules:**

Ansible modules are small programs that perform specific actions on local machines, APIs, or remote hosts

### **Tasks:**

Tasks are individual instructions within a play that call Ansible modules to perform specific actions

### **Collections:**

Ansible collections are bundles of modules, roles, plugins, and other Ansible content that can be easily shared and reused

Collection Structure:

```bash
my_collection/
├── roles/
│   └── my_role/
│       └── tasks/
│           └── main.yml
├── plugins/
│   └── modules/
│       └── my_module.py
└── README.md
```

Playbook example:

```bash
---
- hosts: all
  become: true

  tasks:
    - name: Install Apache HTTP Server
      ansible.builtin.apt:
        name: apache2
        state: present
        update_cache: yes

    - name: Copy index.html to web directory
      ansible.builtin.copy:
        src: index.html
        dest: /var/www/html/
        owner: root
        group: root
        mode: '0644'
```

> Save the above YAML file as webserver-playbook.yml and run it with:

```bash
ansible-playbook -i inventory.ini webserver-playbook.yml
```

✅ Project Title:
Automated Package Installation and NTP Configuration Using Ansible with Roles

💡 What I Did:
Created an Ansible playbook (template.yml) to automate:

Installation of packages on CentOS and Ubuntu systems using yum and apt.

Starting and enabling NTP services (chronyd on CentOS, ntp on Ubuntu).

Copying NTP configuration templates from control to target nodes.

Automatically restarting services when configuration changes.

Creating directories on the target machine.

Defined a detailed inventory file with groupings:

webservers, dbservers, and a combine group with common SSH credentials.

Used an ansible.cfg file for custom behavior (disabling host key checking, logging, etc.).

Included Jinja2 templates for NTP configuration (ntpconf_centos, ntpconf_ubuntu).

Later modularized the playbook using Ansible Roles:

Broke down the playbook into tasks, handlers, vars, and templates.

Made the setup reusable and scalable for larger environments.

📘 What I Learned:
OS-Based Conditional Tasks:
Using when: ansible_distribution == "Ubuntu" to run tasks conditionally based on OS.

Loops in Package Installation:
Efficiently installed multiple packages using loop with package managers.

Handlers and Notifications:
Leveraged handlers to restart services only when configuration files change.

Templating with Jinja2:
Managed custom configuration files using template module with backup options.

Inventory Grouping & Variable Management:
Set up host groups (webservers, dbservers) and managed SSH access using ansible_user and ansible_ssh_private_key_file.

Role-Based Structure:
Learned to organize playbooks using roles for better structure, reusability, and maintenance.


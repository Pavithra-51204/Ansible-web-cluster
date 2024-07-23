# Ansible Web Server Cluster Setup

## Project Description

This project provides a configuration for setting up a web server cluster using Ansible. It includes automation scripts to deploy and configure web servers and a load balancer with HAProxy. This setup helps in managing multiple web servers and distributing traffic efficiently.

## Project Structure

```plaintext
ansible-web-cluster/
├── inventory
├── setup_webservers.yml
├── setup_loadbalancer.yml
├── templates/
│   └── haproxy.cfg.j2
└── files/
    └── index.html

a) inventory: Defines the hosts for the web servers and load balancer.
b) setup_webservers.yml: Ansible playbook for configuring web servers.
c) setup_loadbalancer.yml: Ansible playbook for setting up the HAProxy load balancer.
d) templates/haproxy.cfg.j2: Jinja2 template for HAProxy configuration.
e)files/index.html: Sample web page served by the web servers.

Prerequisites:

i) Ansible installed on your local machine.
ii) Access to the target servers (web servers and load balancer) with SSH.
iii) Python and necessary libraries installed on target servers.

Installation:

1. Clone the repository:
git clone https://github.com/your-username/ansible-web-cluster.git
cd ansible-web-cluster

2. Edit the inventory file:
Update the IP addresses and usernames in the inventory file to match your target servers.

3. Run the Ansible playbooks:
Setup Web Servers:
ansible-playbook -i inventory setup_webservers.yml

Setup Load Balancer:
ansible-playbook -i inventory setup_loadbalancer.yml

Usage:
Ensure SSH Access:
Ensure that you have SSH access to all the servers listed in the inventory file.

Customize Configuration:
Modify the haproxy.cfg.j2 template and index.html file as needed for your specific use case.

Deploy Configuration:
Execute the playbooks as described above to deploy and configure your servers.

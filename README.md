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

Prerequisites
Ansible installed on your local machine.
Access to the target servers (web servers and load balancer) with SSH.
Python and necessary libraries installed on target servers.
Installation
Clone the repository:

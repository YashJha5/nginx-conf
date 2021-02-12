# Architectural Diagram #

![Alt text](Architecture.png?raw=true "Optional Title")
 

# Introduction #

This repo is about how to set up nginx server on nodes and implement CI-CD on nginx configuration files by using Jenkins and Ansible.


# What is this repository for? #

• This repo is to check if nginx is installed on nodes if yes then setting nginx to host "nginx.conf", “site1_index” on node machine.
• If nginx is not installed on node machine then it will install nginx first and then update the nginx configuration file.


# How do I get set up? #

• Create 3 EC2 instances (Ansible Server, Node1, Node2)


# SETUP REQUIRMENTS #

Tools needed for Environment setup:
1. Installed Jenkins on Ansible Server EC2
2. Create webhook between Jenkins and Github
3. Installed Ansible on Ansible Server EC2 
4. Create trust relationship between node machines and Ansible server for ssh connection


# How to Setup Nginx on Node server and change configuration of Nginx by CI-CD #

1. Create Webhook between your Jenkins and Github so if there is any change in configuration of nginx in github repo pipeline will be triggered.
2. Install Ansible on the Ansible Server only.
3. Add node machines private IP on Ansible configuration file 
4. Create changes in github repo, the pipeline will be triggered.
5. That pipeline will trigger Ansible playbook in it.
6. That Ansible playbook will check if there is any package named nginx is installed over there.
7. If yes then it will update the configuration else it will install nginx first and then update the configuration.
8. Then it will restart the nginx server. 
9. The path to nginx configuration file is playbook/roles/assignment/templates/ 


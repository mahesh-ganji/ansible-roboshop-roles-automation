Ansible-Roboshop-Roles-Automation
====================================
Ansible roles for deploying the Infrastructure in AWS and configuring the Roboshop e-commerce application

Deploying ec2 instances and Roboshop Components
============================================================

Use below ansible command to deploy mulitple ec2 instances
==============================================================================

ansible-playbook -i inventory.ini roboshop.yaml -e 'instances=["mongodb","redis","mysql","rabbitmq","catalogue","user","cart","shipping","payment","frontend"]'

To deploy each component of the Roboshop application use below command
===========================================================================

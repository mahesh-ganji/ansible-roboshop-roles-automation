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

ansible-playbook -i inventory.ini components.yaml -e component=mongodb 

Roboshop Roles Directory Structure
============================================================

| Directory | Description |
|-----------|-------------|
| tasks/    |  Contains automation tasks    |
| meta/     |  It manages role dependencies |
| templates/ |  Contains Jinja2 template to generate dynamic configuration files |
| files/     |  Contains static configuration files such as service configuration and repository files
| vars/      |  role specific variables |
| handlers/  |  Used for daemon reload and restarting the service |
| common/    |  Contains reusable tasks across the roboshop components |
| group_vars/ | Contains common variables and sensitive information such as password using (AWS SSM /Secrets Manager) |

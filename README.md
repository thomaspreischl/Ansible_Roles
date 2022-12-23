# Ansible_Roles
In this reposity you can find many ansible roles and playbook examples. Most of them are from my homelab deployment.

## Requirements
You have to install Ansible 2.14 to use all functions of the playbooks

## Running your Deployment

You can run your deployment with the following parameters:

* ansible-playbook YOURPLAYBOOK.YML -i INVENTORYFILE

for example: *ansible-playbook 01-create-vsphere-vms.yml -i /inventory/homelab*

for running in debugmode you can add the parameter *-vvv*


# Description of the Roles and Playbooks

## 01-create_vsphere_vms

You can use this playbook to create multiple VMs in your vSphere / vcenter environment. Add the VMs in the defined section in your inventory file.
In your group_vars file you have to define your settings for the connections, passwords and so on.


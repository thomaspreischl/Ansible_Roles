# Ansible_Roles
In this reposity you can find many ansible roles and playbook examples. Most of them are from my homelab deployment.

## Requirements
You have to install Ansible 2.14 to use all functions of the playbooks

## Running your Deployment

You can run your deployment with the following parameters:

* ansible-playbook YOURPLAYBOOK.YML -i INVENTORYFILE

for example: * ansible-playbook 01-create-vsphere-vms.yml -i /inventory/homelab *

for running in debugmode you can add the parameter * -vvv *


# Description of the Roles and Playbooks

## 01-create_vsphere_vms


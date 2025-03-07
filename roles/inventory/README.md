inventory
=========
```
This role will update the inventory on the Controller
```
Requirements
------------
```
Admin Account on your Ansible Controller
```
Role Variables
--------------
```
inventory_name: AAP Managed Inventory
#
# These variables are set in the vm role
# vm_name: Linux Daily Demo
# vm_region: us-west-1
#
# Set these variables in the job template extra vars
# ansible_python_interpreter: /usr/bin/python3
#
# Credential Types needed for this role
# Amazon Web Services
# Red Hat Ansible Automation Platform
```
Dependencies
------------

Example Playbook
----------------
```
---
- name: Add a VM to your inventory
  hosts: localhost
  connection: local

  tasks:

    - name: Include the inventory role
      tags:
        - inventoryadd
      ansible.builtin.include_role:
        name: inventory

or

---
- name: Remove a vm from our inventory
  hosts: localhost
  connection: local

  tasks:

    - name: Include the vm role
      tags:
        - inventorydel
      ansible.builtin.include_role:
        name: inventory
```
License
-------

https://opensource.org/license/mit
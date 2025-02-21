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
inventory_vm_name: F5 Daily Demo
# Use a Red Hat Ansible Automation Platform credential type
# CONTROLLER_HOST: example.com
# CONTROLLER_USERNAME: mickey.mouse
# CONTROLLER_PASSWORD: password
inventory_managed_inventory_name: AAP Managed Inventory
inventory_region: us-west-1
ansible_python_interpreter: /usr/bin/python3

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
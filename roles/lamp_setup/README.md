lamp_setup
=========
```
This role will setup apache, mysql and php on a linux server
```
Requirements
------------
```
Root access on the machines in the inventory
```
Role Variables
--------------
```
#
# Credential Types needed for this role
# Machine
```
Dependencies
------------

Example Playbook
----------------
```
---
- name: LAMP setup
  hosts: all
  connection: local

  roles:

    - role: lamp_setup
```
License
-------

https://opensource.org/license/mit

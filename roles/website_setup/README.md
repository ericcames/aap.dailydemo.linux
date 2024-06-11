website_setup
=========
```
Sets up our website
```
Requirements
------------
```
Root access on the machines in the inventory
```
Role Variables
--------------

Dependencies
------------

Example Playbook
----------------
```
---
- name: Website setup
  hosts: all
  connection: local

  roles:

    - role: website_setup
```
License
-------

https://opensource.org/license/mit

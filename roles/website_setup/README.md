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
```
ticket_number: 123456
```

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

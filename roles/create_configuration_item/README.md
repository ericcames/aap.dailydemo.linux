create_configuration_item
=========
```
Create a Configuration Management Database (CMDB) Record in ServiceNow
```
Requirements
------------

Role Variables
--------------
```
```
Dependencies
------------

Example Playbook
----------------
```
---
- name: Creates a configuration item
  hosts: localhost
  connection: local

  roles:

    - role: create_configuration_item
```
License
-------

https://opensource.org/license/mit

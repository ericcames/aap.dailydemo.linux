create_cmdb_relationship
=========
```
Create a Configuration Management Database (CMDB) relationship in ServiceNow
```
Requirements
------------

Role Variables
--------------
```
relationship_resource: cmdb_rel_ci
relationship_child: "Ansible Demonstrations"
my_server: aap.example.com
relationship_type: "Uses::Used by"

```
Dependencies
------------

Example Playbook
----------------
```
---
- name: Creates a relatioship
  hosts: localhost
  connection: local

  roles:

    - role: create_cmdb_relationship
```
License
-------

https://opensource.org/license/mit

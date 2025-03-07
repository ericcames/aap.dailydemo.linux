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
create_cmdb_relationship_resource: cmdb_rel_ci
create_cmdb_relationship_child: "Ansible Demonstrations"
create_cmdb_relationship_type: "Uses::Used by"
#
# This is stat in the get_instance_info role
# get_instance_info_server: ''
#
# Credential Types needed for this role
# ServiceNow ITSM Credential - This is a Custom Credential
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

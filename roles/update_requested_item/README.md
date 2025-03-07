update_requested_item
=========
```
Update requested item ticket in ServiceNow
```
Requirements
------------

Role Variables
--------------
```
# These variables are set as Extra Vars
update_requested_item_comments: "Your Comments go here"
update_requested_item_state: 4
#
# Variable set at the workflow template
# ticket_number: ''
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
- name: Update requested item ticket in servicenow
  hosts: localhost

  roles:

    - role: update_requested_item
```
License
-------

https://opensource.org/license/mit

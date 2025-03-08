requested_item_comment
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
requested_item_comment_comments: "Your Comments go here"
#
# Job output
# ansible_success_result.msg
# tower_job_id
# tower_job_template_name
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

    - role: requested_item_comment
```
License
-------

https://opensource.org/license/mit

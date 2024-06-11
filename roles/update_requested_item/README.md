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
requested_item_comments: "Your Comments go here"
requested_item_state: 4
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

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
website_setup_qnr_code: "AmesQNRCode.png"
website_setup_short_url: "https://red.ht/3Z9vKIa"
#
# Variable set at the workflow template
# ticket_number: ''
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
- name: Website setup
  hosts: all
  connection: local

  roles:

    - role: website_setup
```
License
-------

https://opensource.org/license/mit

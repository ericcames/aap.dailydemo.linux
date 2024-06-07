redhat_subscription_manager
=========
```
This role manages your red hat subs with the redhat customer portal
```
Requirements
------------

Role Variables
--------------
```
customer_portal_username: mikey.mouse
customer_portal_password: redhat123
status: present
```
Dependencies
------------

Example Playbook
----------------
```
---
- name: Registering system with Red Hat Subscription Management
  hosts: rheldemo
  gather_facts: no

  roles:

    - role: redhat_subscription_manager
        status: present
```
License
-------

https://opensource.org/license/mit

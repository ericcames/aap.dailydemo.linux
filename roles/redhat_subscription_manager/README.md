redhat_subscription_manager
=========

This role manages your red hat subs with the redhat customer portal

Requirements
------------

Role Variables
--------------

username: mikey.mouse
password: redhat123
status: present

Dependencies
------------

Example Playbook
----------------

---
- name: Registering system with Red Hat Subscription Management
  hosts: rheldemo
  gather_facts: no

  roles:

    - role: redhat_subscription_manager
        status: present

License
-------

https://opensource.org/license/mit

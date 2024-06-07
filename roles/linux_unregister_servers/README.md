linux_unregister_servers
=========
```
This will unregister the server from Insights and the Customer Portal.
```
Requirements
------------

Role Variables
--------------

Dependencies
------------

Example Playbook
----------------
```
---
- name: Linux unregistration
  hosts: all
  connection: local

  roles:

    - role: linux_unregister_servers
```
License
-------

https://opensource.org/license/mit

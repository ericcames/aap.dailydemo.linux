inventory_remove_servers
=========

This role will remove servers from an inventory on your ansible controller

Requirements
------------

Admin Account on your Ansible Controller

Role Variables
--------------

controller_url: example.com
controller_user: mickey.mouse
controller_passwd: password
managed_inventory_name: AAP Managed Inventory

Dependencies
------------

Example Playbook
----------------

---
- name:
  hosts: localhost
  connection: local

  roles:

    - role: inventory_remove_servers

License
-------

https://opensource.org/license/mit
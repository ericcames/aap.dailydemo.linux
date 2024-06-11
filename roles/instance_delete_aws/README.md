instance_delete_aws
=========
```
This role will delete the containerized ansible automation platform.
```
Requirements
------------
```
Amazon Web Console Account
Amazon Web Services Credential in Ansible Automation Platform
```
Role Variables
--------------
```
user_name: mickey.mouse
region: us-west-1
my_email_address: "{{ user_name }}@redhat.com"
```
Dependencies
------------

Example Playbook
----------------
```
---
- name: Delete Ansible Automation Platform deployment
  hosts: localhost
  connection: local

  roles:

    - role: instance_delete_aws
```
License
-------

https://opensource.org/license/mit

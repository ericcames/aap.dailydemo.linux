vm
=========
```
This role will create or delete a vm
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
vm_name: F5 Daily Demo
vm_vpc_name: f5-dailydemo
vm_user_name: eric.ames
vm_subnet_name: "{{ vm_vpc_name }}_Subnet"
vm_image: ami-0a6612e49a32df1e9
vm_count: 1
vm_region: us-west-1
vm_assign_public_ip: true
vm_alwaysup: false
vm_instance_type: m5.xlarge
vm_ec2_security_group_name: "{{ vm_vpc_name }}_SECGRP"
vm_ec2_ansible_group: "{{ vm_user_name }}"
vm_my_email_address: "{{ vm_user_name }}@redhat.com"
vm_my_ssh_key: zigfreed-ssh-key
ansible_python_interpreter: /usr/bin/python3
```
Dependencies
------------

Example Playbook
----------------
```
---
- name: Create our F5 daily demo vm
  hosts: localhost
  connection: local

  tasks:

    - name: Include the vm role
      tags:
        - createvm
      ansible.builtin.include_role:
        name: vm

or

---
- name: Remove our F5 daily demo vm
  hosts: localhost
  connection: local

  tasks:

    - name: Include the vm role
      tags:
        - removevm
      ansible.builtin.include_role:
        name: vm
```
License
-------

https://opensource.org/license/mit

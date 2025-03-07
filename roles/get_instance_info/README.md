get_instance_info
=========
```
This role will gather ec2 info.
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
#
# These variables are set in the vm role
# vm_name: ''
# vm_region: ''
# vm_my_email_address: ''
#
# These stats are used in create_configuration_item role
# get_instance_info_server: ''
# get_instance_info_public_ip: ''
# get_instance_info_ami_id: ''
# get_instance_info_instance_id: ''
# get_instance_info_instance_type: ''
#
# These stats are used in the website_setup role
# get_instance_info_launch_time: ''
# get_instance_info_availability_zone: ''
#
# Set these variables in the job template extra vars
# ansible_python_interpreter: /usr/bin/python3
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
- name: Gather machine info
  hosts: localhost
  connection: local

  roles:

    - role: get_instance_info
```
License
-------

https://opensource.org/license/mit

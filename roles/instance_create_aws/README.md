instance_create_aws
=========
```
This role will create a containerized ansible automation platform.
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
vpc_name: aap_containerized_deployment
user_name: eric.ames
subnet_name: "{{ vpc_name }}_Subnet"
image: ami-06127bea7af8a9ad8
count: 1
region: us-west-1
assign_public_ip: yes
alwaysup: false
instance_type: m5.xlarge
ec2_security_group_name: "{{ vpc_name }}_SECGRP"
ec2_ansible_group: "{{ user_name }}"
my_email_address: "{{ user_name }}@redhat.com"
```
Dependencies
------------

Example Playbook
----------------
```
---
- name: Create AWS VPC for Ansible Automation Platform deployment
  hosts: localhost
  connection: local

  roles:

    - role: instance_create_aws
```
License
-------

https://opensource.org/license/mit

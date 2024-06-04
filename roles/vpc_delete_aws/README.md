vpc_delete_aws
=========

This role will delete an Amazon Virtual Private Cloud (VPC).

Requirements
------------

Amazon Web Console Account
Amazon Web Services Credential in Ansible Automation Platform

Role Variables
--------------

vpc_name: your_vpc_name_goes_here
vpc_cidr: 172.16.3.0/24
region: us-west-1
user_name: first.last
ec2_ansible_group: "{{ user_name }}"
ec2_security_group_name: "{{ vpc_name }}_SECGRP"
ec2_vpc_subnet_name: "{{ vpc_name }}_Subnet"
ec2_rt_name: "{{ vpc_name }}_RT_Internet"
ec2_igw_name: "{{ vpc_name }}_IGW"
my_email_address: "{{ user_name }}@redhat.com"

Dependencies
------------

amazon.aws

Example Playbook
----------------

---
- name: Create AWS VPC for Ansible Automation Platform deployment
  hosts: localhost
  connection: local

  roles:

    - name: vpc_delete_aws

License
-------

https://opensource.org/license/mit

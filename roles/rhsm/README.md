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
rhsm_status: present
rhsm_sat6_fqdn: sat.kona.services
rhsm_org_id: "AmesCO"
rhsm_activation_key: ''
#
# Stat used in website_setup role
# rhsm_subscription_time: ''
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

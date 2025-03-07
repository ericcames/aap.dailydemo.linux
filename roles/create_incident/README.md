create_incident
=========
```
Create a incident ticket in ServiceNow
```
Requirements
------------

Role Variables
--------------
```
create_incident_incident_impact: low
create_incident_incident_urgency: low
create_incident_support_group: "Ansible West Tigers"
create_incident_ticket: ''
#
# Variable set as an Extra Var
create_incident_caller_name: mickey.mouse
#
# Variables set in the vm role
# vm_my_error: ''
# vm_my_job_id: ''
# vm_my_job_template_name: ''
#
# Variable set at the workflow template
# ticket_number: ''
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
- name: Creates an incident ticket in servicenow
  hosts: localhost

  roles:

    - role: create_incident
```
License
-------

https://opensource.org/license/mit

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
caller_name: mickey.mouse
my_job_id: 123456
my_job_template_name: foobar
ticket_number: 654321
incident_impact: low
incident_urgency: low
support_group: "Ansible West Tigers"
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

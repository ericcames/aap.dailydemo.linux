Ansible Automation Platform Daily Demo for Linux
=========
A demo designed to showcase many of the use cases that people are looking for.  We are using the workflow visualizer to show how the various building blocks are put together and enable the delivery on demand of a custom website.  The playbooks call roles, the roles allow for ease of sharing the code and also allow for documentation of the various things needed in each role. The demo is designed to be integrated with an IT Service Management (ITSM) system.  Everything will be documented in ITSM system via the skillfull use of automation.

Day 0 - Configuration as code (CAC) a repeatable build process for this demo
=========
Configuration as code give you an easy way to recover/move your ansible related artifacts to a new platform.  That includes your hardcoded credentials.  The hardcoded credentials can be safely vaulted in an ansible vault file.  Check out the setup_demo.yml for the configurations for setting up this demo using configuration as code.

[Setup - Linux Daily Demo - CAC](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/setup_demo.yml "Setup - Linux Daily Demo - CAC")<br>

Variables used in the setup template
```
my_organization: AmesCO
my_vault: Eric Ames
my_rh_aap_credential: aap.kona.services
my_aws_credential: AWS Blank Open Environment pvwk8
my_aws_machine_credential: AWS Machine Credential - Ames
my_itsm_credential: ServiceNow ITSM Credential - Ames
my_itsm_username: hercules
my_sat_credential: sat.kona.services
timezone_id: America/Phoenix
satellite_host: https://sat.kona.services
remotevault: true
my_remote_vault: >-
  https://raw.githubusercontent.com/ericcames/aap.as.code/refs/heads/main/playbooks/files/vaults/ames/vault_ames.yml
aap_configuration_async_retries: 60
```
# The workflow

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/ddlwf1.png "Start of workflow")
![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/ddlw2.png "Middle of Workflow")
![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/ddlwf3.png "End of Workflow")

**The playbooks**

[1. DDL - VM Create](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/create_instance_02.yml "create_instance_02.yml")<br>
[2. DDL - Inventory Update](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/add_inventory_03.yml "add_inventory_03.yml")<br>
[3. DDL - Get Instance Info](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/get_instance_info_04.yml "get_instance_info_04.yml")<br>
[4. DDL - Red Hat Registration](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/redhat_subscription_manager_05.yml "redhat_subscription_manager_05.yml")<br>
[5. DDL - Configuration Management](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/post_install_06.yml "post_install_06.yml")<br>
[6. DDL - Application Install](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/lamp_setup_08.yml "lamp_setup_08.yml")<br>
[7. DDL - Website deployment](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/website_deployment_09.yml "website_deployment_09.yml")<br>
[Delete Daily Demo Linux clean everything up](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/site_delete.yml "site_delete.yml")<br>

ServiceNow
========

**The playbooks**

[DDL - Create a CMDB record](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/servicenow/create_ci.yml "create_ci.yml") <br>
[DDL - Create CMDB relationship](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/servicenow/create_cmdb_relationship.yml "create_cmdb_relationship.yml") <br>
[DDL - Create Incident](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/servicenow/incident_create.yml "incident_create.yml") <br>
[DDL - Update request ticket -*](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/servicenow/update_sn_req_itm.yml "update_sn_req_itm.yml") <br>

ServiceNow credential<br>
Input configuration
```
fields:
  - id: instance
    type: string
    label: Instance
  - id: username
    type: string
    label: username
  - id: password
    type: string
    label: password
    secret: true
required:
  - instance
  - username
  - password
```
Injector configuration
```
env:
  SN_HOST: '{{instance}}'
  SN_PASSWORD: '{{password}}'
  SN_USERNAME: '{{username}}'
```
- ServiceNow setup

[Event-Driven Ansible Notification Service](https://github.com/shadowman-lab/Ansible-SNOW/tree/main/SNOWSetup#servicenowaap-integration-instructions-using-event-driven-ansible-notification-service "Event-Driven Ansible Notification Service") <br>
[Event-Driven Ansible Event Streams](https://www.youtube.com/watch?v=P2NmuCIUiYg&t=811s "Event-Driven Ansible Event Streams") <br>

- Automated incident management example

[Example Error Handling in support of incident enrichment](https://github.com/ericcames/aap.dailydemo.linux/blob/main/roles/instance_create_aws/tasks/main.yml "Example Error Handling") <br>

# Event Driven Ansible (EDA) Rulebook driving the workflow

- [EDA Rulebook](https://github.com/ericcames/event.driven.ansible/blob/main/rulebooks/servicenow/requested_item.yml "EDA Rulebook")

# The website

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/webtop.png "Webtop")
![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/webmid.png "Webmid")
![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/Webbot.png "Webbottom")

# Cockpit the Administrators GUI

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/cockpit.png "cockpit")

# The command line; there's no place like home :-)

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/cli.png "The command line")

Looking for other Daily Demos?
=========

- [AAP Daily Demo Windows](https://github.com/ericcames/aap.dailydemo.windows "AAP Daily Demo Windows")
- [AAP Daily Demo Linux](https://github.com/ericcames/aap.dailydemo.linux "AAP Daily Demo Linux")
- [AAP Daily Demo F5](https://github.com/ericcames/aap.dailydemo.F5 "AAP Daily Demo F5")
- [AAP Daily Demo Panos](https://github.com/ericcames/aap.dailydemo.Panos "AAP Daily Demo Panos")
- [AAP Daily Demo Satellite](https://github.com/ericcames/aap.dailydemo.satellite "AAP Daily Demo Satellite")

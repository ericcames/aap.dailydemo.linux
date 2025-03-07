Ansible Automation Platform Daily Demo for Linux
=========
A demo designed to showcase many of the use cases that people are looking for.  We are using the workflow visualizer to show how the various building blocks are put together and enable the delivery on demand of a custom website.  The playbooks call roles, the roles allow for ease of sharing the code and also allow for documentation of the various things needed in each role. The demo is designed to be integrated with an IT Service Management (ITSM) system.  Everything will be documented in ITSM system via the skillfull use of automation.

# The workflow

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/DDLWF1.png "Start of workflow")
![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/DDLWF2.png "Middle of Workflow")
![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/DDLWF3.png "End of Workflow")

**The playbooks**

[1. Create our virtual machine](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/create_instance_02.yml "create_instance_02.yml")<br>
[2. Update our inventory](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/add_inventory_03.yml "add_inventory_03.yml")<br>

[3. Gather instance information](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/get_instance_info_04.yml "get_instance_info_04.yml")<br>
[4. Red Hat Registration](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/redhat_subscription_manager_05.yml "redhat_subscription_manager_05.yml")<br>

Red Hat Customer Portal Credential<br>
Input configuration
```
fields:
  - id: user
    type: string
    label: Red Hat Customer Portal Username (access.redhat.com)
  - id: password
    type: string
    label: Red Hat Customer Portal Password
    secret: true
required:
  - user
  - password
```
Injector configuration
```
extra_vars:
  customer_portal_password: '{{password}}'
  customer_portal_username: '{{user}}'
```

[5. Configuration Management](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/post_install_06.yml "post_install_06.yml")<br>
[6. Application install](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/lamp_setup_08.yml "lamp_setup_08.yml")<br>
[7. Website deployment](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/website_deployment_09.yml "website_deployment_09.yml")<br>

[Site Delete will clean everything up](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/site_delete.yml "site_delete.yml")<br>

ServiceNow
========

**The playbooks**

[Create a CMDB record](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/servicenow/create_ci.yml "create_ci.yml") <br>
[Create a CMDB relationship](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/servicenow/create_cmdb_relationship.yml "create_cmdb_relationship.yml") <br>

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/DDLWF2.png "Middle of Workflow")

[Create incident ticket](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/servicenow/incident_create.yml "incident_create.yml") <br>

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/DDLWF1.png "Start of workflow")

[Update requested item ticket](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/servicenow/update_sn_req_itm.yml "update_sn_req_itm.yml") <br>

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

[Ansible spoke setup - Alex Dworjan](https://github.com/shadowman-lab/Ansible-SNOW/tree/master/SNOWSetup#servicenowaap-integration-instructions-using-ansible-spoke "Ansible spoke setup - Alex") <br>
[Ansible spoke youtube - Alex Dworjan](https://www.youtube.com/watch?v=DmPXiRHjgRY "Ansible spoke youtube - Alex Dworjan") <br>

- Automated incident management example

[Example Error Handling in support of incident enrichment](https://github.com/ericcames/aap.dailydemo.linux/blob/main/roles/instance_create_aws/tasks/main.yml "Example Error Handling") <br>

# The website

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/Web01.png "Webtop")
![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/Web02.png "Webbottom")

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

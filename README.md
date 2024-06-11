Ansible Automation Platform Daily Demo for Linux
=========
A demo designed to showcase many of the use cases that people are looking for.  We are using the workflow visualizer to show how the various building blocks are put together and enable the delivery on demand of a custom website.  The playbooks call roles, the roles allow for ease of sharing the code and also allow for documentation of the various things needed in each role. The demo is designed to be integrated with an IT Service Management (ITSM) system.  Everything will be documented in ITSM system via the skillfull use of automation.  Check out the video below to see that "the art of the possible."

# The workflow

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/DDLWF.png "Workflow")

**The playbooks**

[1. Create our network container](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/create_vpc_01.yml "create_vpc_01.yml") <br>
[2. Create our virtual machine](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/create_instance_02.yml "create_instance_02.yml")<br>
[3. Update our inventory](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/add_inventory_03.yml "add_inventory_03.yml")<br>
- Custom Ansible Controller Credential
```
Input configuration

fields:
  - id: url
    type: string
    label: Controller URL
  - id: user
    type: string
    label: Controller Username
  - id: password
    type: string
    label: Controller Password
    secret: true
required:
  - url
  - user
  - password
```
```
Injector configuration

extra_vars:
  controller_url: '{{url}}'
  controller_user: '{{user}}'
  controller_passwd: '{{password}}'
```
[4. Gather instance information](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/get_instance_info_04.yml "get_instance_info_04.yml")<br>
[5. Red Hat Registration](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/redhat_subscription_manager_05.yml "redhat_subscription_manager_05.yml")<br>
[6. Configuration Management](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/post_install_06.yml "post_install_06.yml")<br>
[7. User access](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/provision_user_access_07.yml "provision_user_access_07.yml")<br>
[8. Application install](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/lamp_setup_08.yml "lamp_setup_08.yml")<br>
[9. Website deployment](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/website_deployment_09.yml "website_deployment_09.yml")<br>
[10. Send notification that the website is ready](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/sendmail_10.yml "sendmail_10.yml")<br>
- Custom Mail Server credential
```
Input configuration

fields:
  - id: smtp_server
    type: string
    label: Mail Server
  - id: smtp_port
    type: string
    label: Mail Server Port
  - id: smtp_username
    type: string
    label: Mail Server Username
  - id: smtp_password
    type: string
    label: Mail Server Password
    secret: true
required:
  - smtp_server
  - smtp_port
  - smtp_username
  - smtp_password
```
```
Injector configuration

extra_vars:
  MAILHOST: '{{smtp_server}}'
  MAILHOST_PORT: '{{smtp_port}}'
  MAILHOST_PASSWORD: '{{smtp_password}}'
  MAILHOST_USERNAME: '{{smtp_username}}'
```
[Site Delete will clean everything up](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/site_delete.yml "site_delete.yml")<br>

**The ServiceNow directory**

[Create a CMDB record](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/servicenow/create_ci.yml "create_ci.yml") <br>
[Create a CMDB relationship](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/servicenow/create_cmdb_relationship.yml "create_cmdb_relationship.yml") <br>

# The website

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/DDLW1.png "Webtop")
![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/DDLW2.png "Webbottom")

# A youtube video of the demo

- [AAP Daily Demo Linux](https://youtu.be/Wvf7-CZmAHI?si=oxqDRAWsfqpXTnD- "AAP Daily Demo Linux")

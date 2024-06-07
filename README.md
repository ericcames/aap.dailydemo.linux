Ansible Automation Platform Daily Demo for Linux
=========
A demo designed to showcase many of the use cases that people are looking for.  We are using the workflow visualizer to show how the various building blocks are put together and enable the delivery on demand of a custom website.  The playbooks call roles, the roles allow for ease of sharing the code and also allow for documentation of the various things needed in each role. The demo is designed to be integrated with an IT Service Management (ITSM) system.  Everything will be documented in ITSM system.  Check out the video below to see that "the art of the possible."

# The workflow

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/DDLWF.png "Workflow")

**The playbooks**

- [1. Create our network container](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/create_vpc_01.yml "create_vpc_01.yml")
- [2. Create our virtual machine](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/create_instance_02.yml "create_instance_02.yml")
- [3. Update our inventory](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/add_inventory_03.yml "add_inventory_03.yml")
- [4. Gather instance information](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/get_instance_info_04.yml "get_instance_info_04.yml")
- [5. Red Hat Registration](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/redhat_subscription_manager_05.yml "redhat_subscription_manager_05.yml")
- [6. Configuration Management](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/post_install_06.yml "post_install_06.yml")
- [7. User access](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/provision_user_access_07.yml "provision_user_access_07.yml")
- [8. Application install](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/lamp_setup_08.yml "lamp_setup_08.yml")
- [9. Website deployment](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/website_deployment_09.yml "website_deployment_09.yml")
- [10. Send notification that the website is ready](https://github.com/ericcames/aap.dailydemo.linux/blob/main/playbooks/sendmail_10.ym "sendmail_10.yml")


# The website

![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/DDLW1.png "Webtop")
![alt text](https://github.com/ericcames/aap.dailydemo.linux/blob/main/images/DDLW2.png "Webbottom")

# A youtube video of the demo

- [AAP Daily Demo Linux](https://youtu.be/Wvf7-CZmAHI?si=oxqDRAWsfqpXTnD- "AAP Daily Demo Linux")

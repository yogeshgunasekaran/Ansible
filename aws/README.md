
# This ansible-playbook is to manage aws services. To generate and setup aws keypair and one ec2 instance in aws from ansible control machine

## Prerequisite

### Installation and provisioning of ansible control machine 

#### In AWS :
- AMI - Ubuntu 20.04 LTS
- Security Group,
    * Allow **port 22**, source: **My IP** - to ssh into ansible control machine from My IP
- **IAM &rarr; users &rarr; Add users**. Set username as **ansibleadmin** and choose aws credential type as **Access key - Programmatic access**. Attach existing policies directly with **AdministratorAccess**. Save the accesskey and secretkey.

 #### In Ansible control machine :
 - Login to a non-root **admin user**
 - [Click here for installation of anbile in the control machine](https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html#installing-ansible-on-ubuntu)
 - [Export the environmental variables](https://docs.ansible.com/ansible/2.5/scenario_guides/guide_aws.html#authentication) of aws accesskey and secretkey in **.bashrc file** at the bottom line
  ```sh 
  vim .bashrc 
  ````
   ```sh 
  source .bashrc 
  ````


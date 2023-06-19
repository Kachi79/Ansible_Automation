# Ansible_Automation

![](./img/1.a.architecture.png)

## Installing Ansible on Jenkins Server
We install ansible on our jenkins server and rename it to `Jenkins-Ansible`

```
sudo apt update

sudo apt install ansible
```

![](./img/3.a.%20jenkins-server.jpg)
#

Create a new repository called `ansible-config-mgt` on github and set up webhooks on it.

`https://<jenkins_url:port/github-webhooks>`

On the Jenkins server, create a job called `ansible` and configure automatic builds when a trigger is made on the `ansible-config-mgt` directory via GITScm polling.

![](./img/3.b.webhooks.jpg)

Test configuration by updating a README file on github.
![](./img/3.configure_webhook_to_jenkins.jpg)

## Prepare Development using VSCode
#
Download and install vscode which will be used to write and edit code.

## Ansible Configuration
#
Clone `ansible-config-mgt` repo on local machine and create a new branch for development 
![](./img/4.new_branch.jpg)

- Create a playbooks directory for storing playbooks
- Create an inventory directory for storing inventory files
- In the playbooks folder, create a common.yml file
- In the inventory folder, create dev.yml, prod.yml, staging.yml and uat.yml for dev, prod, staging and uat environments respectively.

![](./img/4.a.directories.jpg)


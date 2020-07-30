# Challenge 5 - Configure a Linux Server with NGINX

[< Previous Challenge](./Challenge-04.md) - [Home](../readme.md) - [Next Challenge>](./Challenge-06.md)

## Introduction

The goals for this challenge include understanding:
- Custom script extensions
- Globally unique naming context and complex dependencies
- Staging artifacts in a location accessible to the Azure Resource Manager

## Description

We have provided a script (`install_apache.sh`) that configures a web server on a Linux VM. When run on the VM, the script deploys a static web page that should be available at `http://<PublicIPofTheVM>/wth.html`

You can find the script in the Resources folder for **Challenge-06**.

Your challenge is to:

- Extend the Ansible playbook to configure a webserver on the Linux VM you deployed
    - Host the script file in a secure artifact (staging) location that is only accessible to the Azure Resource Manager.
    - Pull the website configuration script from the artifact location.

```
ORIGINAL CHALLENGE TEXT

Install the NGINX web server on an existing Linux Virtual Machine. To do this you will need to create an inventory.cfg and a YAML file. The inventory.cfg has information about the VM you want to manage and the location of the Python interpreter. To find the location of Python, you will need to SSH to the VM and look in /usr/bin. Use the latest version

It should look something like this:

[web]
{Your public IP address of the Linux VM} ansible_user=azureuser

[web:vars]
ansible_python_interpreter={location of python install}

Once you have the inventory.cfg, you will create the Ansible Playbook YAML file that will install NGINX. First, you will update all apt (Ubuntu) or yum (Redhat/CentOS) packages to the latest version. For RedHat/CentOS you will need install the EPEL repository (epel-release) before we install NGINX. Next, you will install NGINX using apt or yum in the file and set the service to running.

To use the inventory.cfg file you will need to run the following Ansible playbook command which will use the inventory.cfg and YAML file you created earlier. The -b switch tells Ansible to run as root using sudo.

ansible-playbook -i inventory.cfg {yaml file} -b

```

## Success Criteria

1. Verify that NGINX is running by running curl from the SSH terminal with `curl http://127.0.0.1`

## Tips

- Use an Azure Blob Storage account as the artifact location
- Secure access to the artifact location with a SAS token
- Pass these values to the Ansible playbook as parameters
# Challenge 5 - Configure a Linux Server with NGINX

[< Previous Challenge](./Challenge-04.md) - [Home](../readme.md) - [Next Challenge>](./Challenge-06.md)

## Introduction

The goals for this challenge include understanding:
- Custom script extensions
- Globally unique naming context and complex dependencies
- Staging artifacts in a location accessible to the Azure Resource Manager

## Description

Your challenge is to:

Install the NGINX web server on an existing Linux Virtual Machine and replace the home page. To do this you will need to create an inventory.cfg and a YAML file. The inventory.cfg has information about the VM you want to manage and the location of the Python interpreter. To find the location of Python, you will need to SSH to the VM and look in /usr/bin. Use the latest version. 

It should look something like this:

[web]
{Your public IP address of the Linux VM} ansible_user=azureuser

[web:vars]
ansible_python_interpreter={location of python install}

Once you have the inventory.cfg, you will create the Ansible Playbook YAML file that will install NGINX. First, you will update all apt (Ubuntu) or yum (Redhat/CentOS) packages to the latest version. You will install NGINX using apt or yum in the YAML file and set the service to running. 

To use the inventory.cfg file you will need to run the following Ansible playbook command which will use the inventory.cfg and YAML file you created earlier. The -b switch tells Ansible to run as root using sudo.

ansible-playbook -i inventory.cfg {yaml file} -b


## Success Criteria

1. Verify that NGINX is running by opening your browser and navigating to http://<public IP Address>/wth.html

## Hint

You can use echo to emit HTML to replace the default home page. For example, for Ubuntu it would be:

echo \<center\>\<h1\>Welcome to What The Hack: IaC Ansible Challenges\</h1\>\<br/\>\</center\> > /usr/share/nginx/html/wth.html

## Tips

For RedHat/CentOS you will need install the EPEL repository (epel-release) before we install NGINX.
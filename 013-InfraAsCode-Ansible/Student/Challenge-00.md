# Challenge 0 - Getting Your Machine Ready

[< Home](../readme.md)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Next Challenge>](./Challenge-01.md)

## Pre-requisites

## Install and Configure Ansible
You have several options to choose from when in comes to installing Ansible.

1) Install Ansible on your own machine. On Windows you can use the Windows Subsystem for Linux and a Linux distribution like Ubuntu from the Microsoft Store. You can also install Ansible on Mac OS or Linux.
2) Use Azure Cloud Shell which already has Ansible installed

Using Azure Cloud Shell is the quickest method but you may wish to have more control of your editor and so one of the other options may be more desirable for you.

You will need to create Azure credentials using your Azure subscription ID and service principal values. Once you have done that you will create an Ansible credentials file with your subscription Id, tenant Id, secret and client Id. 

You may also want to use Visual Studio Code which is available on Windows, Mac and Linux for editing the YAML files needed for Ansible. You can add the Ansible and the YAML extensions for this. 

## Create SSH Key

Generate an SSH key pair for being able to access your Linux VM's. You can find a detailed instructions on how to create an SSH key pair at the URL below. 

https://docs.microsoft.com/en-us/azure/virtual-machines/linux/create-ssh-keys-detailed

## Learning Resources
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#selecting-an-ansible-version-to-install 
https://docs.microsoft.com/en-us/azure/virtual-machines/linux/ansible-install-configure#install-ansible-on-an-azure-linux-virtual-machine
https://docs.ansible.com/ansible/latest/scenario_guides/guide_azure.html#providing-credentials-to-azure-modules
https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal



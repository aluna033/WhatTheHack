# Challenge 4 - Deploy a Virtual Machine

[< Previous Challenge](./Challenge-03.md) - [Home](../readme.md) - [Next Challenge>](./Challenge-05.md)

## Introduction 

In this challenge, you will put all the pieces together and extend your Ansible playbook to deploy a Virtual Machine in Azure.

The goals for this challenge include understanding:
   + Globally unique naming context and complex dependencies
   + Clean code with neat parameter and variable values
   + Figuring out what Azure resources it takes to build a VM

## Description

+	Extend your Ansible playbook to deploy a virtual machine
    +   VM requirements -
        +   Linux OS 
        +   Use a secure secret value for the admin password from Azure Key Vault
    + Use a resource prefix and playbook variables to have consistent naming of resources

```
ORIGINAL CHALLENGE TEXT:

Create a Linux VM using Ansible. You will first need to create a Network Interface Card. Use the following settings for the NIC:

Resource group: ansible-rg Name: ansible-VM-nic Public IP address: ansible-pip VNet: WTHVNETAN Subnet: default Security Group: ansible-nsg-ssh

The VM will use all of the Azure resources you have previously created. Use the following settings:

VM Name: anlinuxvm01 Resource Group: ansible-rg VM Size: Standard_DS1_v2 Admin username: azureuser SSH password enabled: false SSH public keys: [use the public key you created in the prequisites section] Network interfaces: ansible-VM-nic Managed Disk Type: Premium_LRS Image: CentOS 7.5 (or Ubuntu 18.04 if you prefer)

Ensure that you can SSH to the VM using its public IP address with ssh azureuser@[public ip address]

Hint: You can use the Azure CLI command az vm list-ip-addresses to find the IP address for the newly created VM.
```
## Success Criteria

1. Verify that your virtual machine has been deployed via the Azure Portal or Azure CLI.
1. Connect to your virtual machine and verify you can login via SSH

## Tips

- **TIP:** For a Linux VM, you can use an admin password or an SSH key to control access to the VM. It is common (and a recommended practice) to use an SSH key with Linux instead of an admin password. If you are not familiar with Linux, we recommend using an admin password for this hack to keep things simple and focus on learning Ansible playbooks.
- **TIP:** You will need to supply your VM with a Public IP address or use the Azure Bastion service to connect to it.
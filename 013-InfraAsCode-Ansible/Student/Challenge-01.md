# Challenge 1 - Create an Azure Resource Group Using Ansible

 [Home](../readme.md) - [Next Challenge>](./Challenge-02.md)

## Pre-requisites

Make sure your machine is set up with the proper tooling: [What The Hack - Common Prerequisites](../../000-HowToHack/WTH-Common-Prerequisites.md)

There are two ways to use Ansible with Azure:
- Ansible client on your workstation
- Ansible client in Azure Cloud Shell

Ansible is pre-installed in Azure Cloud Shell where it is pre-configured to be authenticated with your Azure subscription.  

If you run Ansible on your workstation, you will need to configure it to authenticate with your Azure subscription. This is part of the challenge.

## Introduction

Your first challenge is to create a simple "Hello World" Ansible playbook. The goals here are to understand:

- How to configure and authenticate Ansible with your Azure subscription
- Core elements of an Ansible playbook and the different ways to deploy it.
- How & where to see and troubleshoot deployments in the portal

## Description

Develop an Ansible playbook that creates an Azure resource group named "ansible-rg"
   - Deploy it using the Azure Cloud Shell
   - Deploy it using Ansible on your workstation


`ORIGINAL CHALLENGE TEXT: Create a YAML file named rg.yml. Using Ansible and the YAML file you created, create a resource group named ansible-rg in the East US 2 Azure region. Deploy the resource group using ansible-playbook`

## Success Criteria

1. You can deploy the playbook from either the Azure Cloud Shell or your workstation
1. You can view the resource group in the Azure Portal

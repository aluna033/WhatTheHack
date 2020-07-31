# Challenge 2 - Deploy a Virtual Network

[< Previous Challenge](./Challenge-01.md) - [Home](../readme.md) - [Next Challenge>](./Challenge-03.md)

## Introduction

This challenge has you add to the "hello world" Ansible playbook you created in the previous challenge. The goals for this challenge include understanding:
   + Parameters and Parameter Files
   + How to find syntax for an Azure resource and add it to the playbook

## Description

Extend the Ansible playbook to provision an Azure Virtual Network. The virtual network should have an address space of 10.2.0.0/16 and be named "wth-vnet-an". Add one subnet to it with an address range of 10.2.0.0/24 and name it "default" 
-	The playbook should take the following as input values: 
    - Virtual Network Name
    - Virtual Network Address Prefix
    - Subnet Name
    - Subnet Address Prefix
-   Use a parameter file to pass in parameter values 

## Success Criteria

1. Verify that Virtual Network has been deployed in the portal
1. Verify that the Virtual Network is configured as per the variable values passed in to the Ansible playbook from the parameter file

## Learning Resources

Learn how to "fish" for Ansible Azure resource syntax:

`Consider adding similar resource links as the ARM template hack examples below`

- [ARM Tools VS Code Extention](https://marketplace.visualstudio.com/items?itemName=msazurermtools.azurerm-vscode-tools)
- [ARM Template Reference docs](https://docs.microsoft.com/en-us/azure/templates)
- Export template from Azure Portal before resource creation
- Export template from Azure Portal of existing Resource Group deployment
- [Azure Quickstart Templates on GitHub](https://github.com/Azure/azure-quickstart-templates)
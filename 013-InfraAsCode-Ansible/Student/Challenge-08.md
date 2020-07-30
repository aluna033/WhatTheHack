# Challenge 8 - Nested Playbooks

[< Previous Challenge](./Challenge-07.md) - [Home](../readme.md) - [Next Challenge>](./Challenge-09.md)

## Introduction

The goals for this challenge include understanding:
- Linked Ansible playbooks allow for granular resource management and deployment
- Staging artifacts in a location accessible to the Azure Resource Manager

An application may require the composition of many underlying infrastructure resources in Azure. As you have now seen with just a single VM and its dependencies, an Ansible playbook can grow large rather quickly.

When playbooks get big, they become monoliths. They are hard to manage.  By breaking your playbook up into smaller linked playbooks, you can achieve more flexibility in how you manage your deployments.

In many companies, deployment of cloud infrastructure may be managed by different teams. For example, a common network architecture and its security settings may be maintained by an operations team and shared across multiple application development teams.

The network architecture and security groups are typically stable and do not change frequently. In contrast, application deployments that are deployed on the network may come and go.

## Description

In this challenge you will separate your existing Ansible playbook into two sets of linked playbooks. 

- Separate networking resources (Virtual Network & Network Security Groups) in to their own template.
- Separate the load balancer, VMs, and its dependencies into their own playbook
- Create a new playbook that deploys each of the new sub-playbooks.
- Ensure parameters flow through from the new playbook to each of the sub-playbooks

By separating the networking resources into their own playbook, an application team can test its infrastructure deployment in a test network. At a later point in time, the linked networking playbook can be replaced with a production playbook provided by the company's operations team.

## Success Criteria

1. Verify that all resources deploy as before when you had a single Ansible playbook

## Learning Resources

`TODO: find comparable ansible resource links`

- [Using linked and nested templates when deploying Azure resources](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/linked-templates)

# Challenge 3 - Open Some Ports

[< Previous Challenge](./Challenge-02.md) - [Home](../readme.md) - [Next Challenge>](./Challenge-04.md)

## Introduction

The goals for this challenge include understanding:
 - variables
 - dependencies (**Hint:** Resource IDs)
 - idempotency

## Description

Extend the Ansible playbook to add a Network Security Group that you will use to protect an Azure VM so that it is only accessible via TCP ports 22 and 80 inbound. Apply the security group to the subnet you created in Challenge 2.

## Success Criteria

1. Verify in the Azure portal Network Security Group has been configured as per the values specified above
1. Verify in the Azure portal that the Network Security has been applied to the subnet

## Learning Resources

`Are resource IDs relevant in the context of Ansible?  If not, this link might not be relevant.`

- [Understanding ARM Resource IDs](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/template-functions-resource#resourceid)
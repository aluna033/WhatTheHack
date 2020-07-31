# Challenge 3 - Open Some Ports

[< Previous Challenge](./Challenge-02.md) - [Home](../readme.md) - [Next Challenge>](./Challenge-04.md)

## Introduction

The goals for this challenge include understanding:
 - variables
 - idempotency

## Description

Extend the Ansible playbook to add a Network Security Group that you will use to protect an Azure VM so that it is only accessible via TCP ports 22 and 80 inbound. Apply the security group to the subnet you created in Challenge 2.

## Success Criteria

1. Verify in the Azure portal Network Security Group has been configured as per the values specified above
1. Verify in the Azure portal that the Network Security has been applied to the subnet

## Learning Resources

https://docs.microsoft.com/en-us/azure/virtual-network/manage-network-security-group

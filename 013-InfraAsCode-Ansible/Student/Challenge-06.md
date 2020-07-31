
# Challenge 6 - Add a Data Disk and mount to OS

[< Previous Challenge](./Challenge-05.md) - [Home](../readme.md) - [Next Challenge>](./Challenge-07.md)

## Introduction

In this challenge you will learn how to configure persistant storage on an Azure VM.

The goals for this challenge include understanding:
- Persistent storage for an Azure VM
- How to apply configuration changes to a Linux server with Ansible

## Description

-	Extend Ansible playbook to:
    - Add a data disk to the Linux VM
    - Partition, format and mount the disk as a data drive in the Linux OS. The Ansible playbook for this has been provided to you. 
    

## Success Criteria

1. Verify you can access the storage disk within the OS

## Learning Resources

- [Add a disk to a Linux VM](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/add-disk)
- [Format a disk in Ansible](https://docs.ansible.com/ansible/latest/modules/filesystem_module.html)


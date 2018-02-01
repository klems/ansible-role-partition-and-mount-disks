klems.partition-and-mount-disks
=========

[![Build Status](https://travis-ci.org/klems/ansible-role-partition-and-mount-disks.svg?branch=master)](https://travis-ci.org/klems/ansible-role-partition-and-mount-disks)

A role to partition and mount a list of hard drives disks with automatic UUID detection.

Requirements
------------
Ansible == `2.4`

Role Variables
--------------
See vars/main.yml for the list of required variables

Dependencies
------------
N/A

Example Playbook
----------------
```
- hosts: servers
  roles:
     - { role: klems.partition-and-mount-disks }
```

License
-------
BSD

Author Information
------------------
mail: klems@klems.net

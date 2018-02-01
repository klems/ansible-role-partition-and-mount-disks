klems.partition-and-mount-disks
=========

[![Build Status](https://travis-ci.org/klems/ansible-role-partition-and-mount-disks.svg?branch=master)](https://travis-ci.org/klems/ansible-role-partition-and-mount-disks)

A role to partition and mount a list of hard drives disks with automatic UUID detection.

Requirements
------------
Ansible == `2.4`

Role Variables
--------------
### {{ additional_disks }}

A list of dictionnaries that must contains the following entries :

```
additional_disks:
  - disk: /dev/sda
    number: 1
    state: present
    part_start: "0%"
    part_end: "100%"
    fstype: ext4
    mount_path: "/mnt/storagebox-01"
    mount_state: mounted
    mount_opts: noatime
  - disk: /dev/sdb
    number: 1
    state: present
    part_start: "0%"
    part_end: "100%"
    fstype: ext4
    mount_path: "/mnt/storagebox-02"
    mount_state: mounted
    mount_opts: noatime
```

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

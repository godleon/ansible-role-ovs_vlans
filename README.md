[![Build Status](https://travis-ci.org/godleon/ansible-role-ovs_vlans.svg?branch=master)](https://travis-ci.org/godleon/ansible-role-ovs_vlans)


Role Name
=========

**godleon.ovs_vlans**

Requirements
------------

### Software

- Python2.7 (**Ubuntu Xenial**)
> sudo apt-get update && sudo apt-get -y install python2.7


Role Variables
--------------

These variables shown below have to be configured before executing the Ansible role:

```yml

ovs_vlans:
  # Physical network interface name which Open vSwitch binds with
  OvsBindingInterface: 'eth0'

  # OVS bridge name
  OvsBridgeName: 'ovsbr0'

  # VLANs which are supported in the OVS bridge
  TrunkVlans: [101, 102, 103, 104, 105]
```

Dependencies
------------

- godeon.kvm_host

> ansible-galaxy install godleon.kvm_host


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
- hosts: servers
  roles:
    - { role: godleon.kvm_host }
    - { role: godleon.ovs_vlans }
```

License
-------

MIT

Author Information
------------------

**Leon Tseng** 

-  [godleon@GitHub](https://github.com/godleon)

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

```yml
# Physical network interface name which Open vSwitch binds with
ovs_vlans_OvsBindingInterface: 'eth0'

# OVS bridge name
ovs_vlans_OvsBridgeName: 'ovsbr0'

# VLANs which are supported in the OVS bridge
ovs_vlans_TrunkVlans: [101, 102, 103, 104, 105]
```

Dependencies
------------

None


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
- hosts: servers
  roles:
    - { role: godleon.ovs_vlans }
```

License
-------

MIT

Author Information
------------------

**Leon Tseng** 

-  [godleon@GitHub](https://github.com/godleon)

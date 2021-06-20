Role: ESXi USB Install
==================

Ansible role to automate the installation of ESXi on usb flash drives. Inspired by William Lam's article, [Automated ESXi Installation to USB using Kickstart](https://williamlam.com/2019/07/automated-esxi-installation-to-usb-using-kickstart.html)

Requirements
------------

- one or more usb flash drives
- ESXi installer iso
- macOS

Role Variables
--------------

Variables with a value of `[]` need to be defined by using either `vars:` in a corresponding playbook or `--extra-vars` on the command line.

Variable | Default Value | Description
| - | - | - |
`unetbootin_install` | `true` | whether or not to install unetbootin
`unetbootin_folder` | `[]` | path to folder containing unetbootin cli
`usb_base_name` | `usb` | base name to assign usb flash drives
`usb_to_create` | `3` | number of ESXi bootable usb flash drives to create
`usb_ports_available` | `3` | number of usb ports available on the target machine
`esxi_base_hostname` | `esxi` | base name to assign ESXi hosts
`esxi_ip_address` | `[192.168.1.11, 192.168.1.12, 192.168.1.13]` | list of ip addresses to assign ESXi hosts
`esxi_netmask` | `255.255.255.0` | netmask to assign ESXi hosts
`esxi_gateway` | `192.168.1.1` | gateway to assign ESXi hosts
`esxi_nameserver` | `192.168.1.1` | nameserver (DNS) to assign ESXi hosts
`esxi_root_password` | `VMware1!` | root password to assign ESXi hosts
`esxi_license_key` | `[]` | (optional) license key to assign ESXi hosts
`esxi_iso_folder` | `'{{ playbook_dir }}/iso'` | path to folder containing ESXi iso; defaults to a folder called 'iso' in the playbook directory that calls this role

Dependencies
------------

N/A

Example Playbook
----------------

```yaml
- hosts: localhost
  connection: local
  
  roles:
    - bendwyer.vmware.esxi_usb_install
```

Additional Information
----------------------

Example extra-vars files can be found in `/files`.

License
-------

MIT

Author Information
------------------

Ben Dwyer  
https://github.com/bendwyer

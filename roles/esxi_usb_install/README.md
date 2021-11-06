Role: ESXi USB Install
==================

Ansible role to automate the installation of ESXi using usb flash drives. Inspired by William Lam's article, [Automated ESXi Installation to USB using Kickstart](https://williamlam.com/2019/07/automated-esxi-installation-to-usb-using-kickstart.html)

- Due to changes in ESXi 7.0U3a, this role **does not** install ESXi to the flash drive. Instead it will install ESXi to the first available local disk.
- If you are using Secure Boot, then the `%firstboot` sections in `KS.CFG` will not run. More information can be found in [Using ESXi Kickstart %firstboot with Secure Boot](https://williamlam.com/2018/06/using-esxi-kickstart-firstboot-with-secure-boot.html), but the easiest fix is to disable Secure Boot while running the installation.

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
`esxi_domain_suffix` | `homelab.internal` | custom domain suffix to assign ESXi hosts
`esxi_vlan` | `[]` | (optional) vlan to assign the management network
`esxi_ip_address` | `[192.168.1.11, 192.168.1.12, 192.168.1.13]` | list of ip addresses to assign ESXi hosts
`esxi_netmask` | `255.255.255.0` | netmask to assign ESXi hosts
`esxi_gateway` | `192.168.1.1` | gateway to assign ESXi hosts
`esxi_nameserver` | `192.168.1.1` | nameserver (DNS) to assign ESXi hosts
`esxi_root_password` | `VMware1!` | root password to assign ESXi hosts
`esxi_license_key` | `[]` | (optional) license key to assign ESXi hosts
`esxi_ssh_enable` | `true` | enables or disables SSH
`esxi_shell_enable` | `true` | enables or disables ESXi shell
`esxi_disable_ipv6` | `true` | disables or enables IPv6
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

- Example extra-vars files can be found in `/files`. Call an exta-vars file using `--extra-vars "@evars_filename.yml"`.

- More information about the commands used in `KS.CFG` can be found at [Installation and Upgrade Script Commands](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.esxi.upgrade.doc/GUID-61A14EBB-5CF3-43EE-87EF-DB8EC6D83698.html) on the VMware documentation website.

License
-------

MIT

Author Information
------------------

Ben Dwyer  
https://github.com/bendwyer

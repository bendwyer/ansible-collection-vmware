=============================
Bendwyer.Vmware Release Notes
=============================

.. contents:: Topics


v1.0.2
======

Release Summary
---------------

Added variables for VLAN and domain name.
Updated searched-for iso pattern.

Minor Changes
-------------

- esxi_usb_install - add new vars to defaults/main.yml (https://github.com/bendwyer/ansible-collection-vmware/pull/5)
- esxi_usb_install - add new vars to evars_macosx.yml (https://github.com/bendwyer/ansible-collection-vmware/pull/5)
- esxi_usb_install - add options for VLAN and domain name to KS.CFG.j2 (https://github.com/bendwyer/ansible-collection-vmware/pull/5)
- esxi_usb_install - update README.md to include new variables (https://github.com/bendwyer/ansible-collection-vmware/pull/5)

Bugfixes
--------

- esxi_usb_install - edit construct.yml iso pattern to be a little more flexible (https://github.com/bendwyer/ansible-collection-vmware/pull/5)

v1.0.1
======

Release Summary
---------------

Fixed typos in README and galaxy.yml files.

Bugfixes
--------

- README - Fix incorrect 'vmwawre' (https://github.com/bendwyer/ansible-collection-vmware/pull/3)
- galaxy.yml - Fix incorrect 'vmwawre' (https://github.com/bendwyer/ansible-collection-vmware/pull/3)

v1.0.0
======

Release Summary
---------------

Initial release.

Minor Changes
-------------

- LICENSE - Create LICENSE (https://github.com/bendwyer/ansible-collection-vmware/pull/1)

New Roles
---------

- bendwyer.vmware.esxi_usb_install - Ansible role to automate the installation of ESXi on usb flash drives.

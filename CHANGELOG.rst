=============================
bendwyer.vmware Release Notes
=============================

.. contents:: Topics


v1.0.4
======

Release Summary
---------------

Release Date: 2021-11-06

Minor Changes
-------------

- esxi_usb_install - add new vars to defaults/main.yml (https://github.com/bendwyer/ansible-collection-vmware/pull/9)
- esxi_usb_install - clean up KS.CFG.j2 templating, add new variables and conditions (https://github.com/bendwyer/ansible-collection-vmware/pull/9)
- esxi_usb_install - update README.md to include new variables (https://github.com/bendwyer/ansible-collection-vmware/pull/9)

Bugfixes
--------

- esxi_usb_install - fix esxi_license_key in defaults/main.yml (https://github.com/bendwyer/ansible-collection-vmware/pull/9)

v1.0.3
======

Release Summary
---------------

Release Date: 2021-11-05

Minor Changes
-------------

- bendwyer.vmware - add meta/runtime.yml file with minimum required Ansible version (https://github.com/bendwyer/ansible-collection-vmware/pull/7)

v1.0.2
======

Release Summary
---------------

Release Date: 2021-11-05

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

Release Date: 2021-06-21

Bugfixes
--------

- README - Fix incorrect 'vmwawre' (https://github.com/bendwyer/ansible-collection-vmware/pull/3)
- galaxy.yml - Fix incorrect 'vmwawre' (https://github.com/bendwyer/ansible-collection-vmware/pull/3)

v1.0.0
======

Release Summary
---------------

Release Date: 2021-06-20

Minor Changes
-------------

- LICENSE - Create LICENSE (https://github.com/bendwyer/ansible-collection-vmware/pull/1)

New Roles
---------

- bendwyer.vmware.esxi_usb_install - Ansible role to automate the installation of ESXi on usb flash drives.

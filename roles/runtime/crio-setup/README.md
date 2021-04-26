crio-setup
=========

This role is used to install CRI-O as container runtime engine either in RedHat or Debian Distro.

Role Variables
--------------

Only need to mention the os family name, for this it depends on another role `os-facts`.

    ansible_os_family: ""

Dependencies
------------

This role used one module `community.general.modprobe`. To use this module, it depends on another ansible collection.

    community.general

For install it use:

    ansible-galaxy collection install community.general

Or install it using requirement file, run:

    ansible-galaxy collection install -r requirements.yml

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: runtime/crio-setup }



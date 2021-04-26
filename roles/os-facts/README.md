os-facts
=========

As this collection is working for multiple OS, this role works as dependency for multiple roles in this collection.

Role Variables
--------------

This role run as a dependency to set facts for OS Distro, used in other roles.

    ansible_os_family

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: os-facts }


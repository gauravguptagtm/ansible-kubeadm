common
=========

This role is used for installing software related to kubernetes cluster setup.

Requirements
------------

None.

Role Variables
--------------

	ansible_os_family: ""

This variable is defined from other role(roles/os-facts).

Dependencies
------------

This role is dependent on other role `os- for variable `ansible_os_family` 

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: common }


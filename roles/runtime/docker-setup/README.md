docker-setup
===========

This role helps in installing docker software as container runtime either in RedHat or Debian Distro.

Role Variables
--------------

This role works fine for both redhat and debian distro, so to set os family name, we need to mention it...

    ansible_os_family: ""

Dependencies
------------

This role is dependent on `os-facts` to get the value of `ansible_os_family`.
 
Example Playbook
----------------

    - hosts: all
      roles:
         - { role: runtime/docker-setup, ansible_os_family: "RedHat" }


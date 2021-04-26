CNI
=========

This role is used for installing container network plugin in kubernetes cluster.

Requirements
------------

You must have kubernetes cluster ready. If not, then run `roles/master` first, then run this role to install CNI Plugin.

Role Variables
--------------

Available variables are listed below, along with default values:

	network: ""

Must use either `flannel` or `weave` in network variable.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: master
      roles:
         - { role: cni, network: "flannel" }

License
-------

BSD


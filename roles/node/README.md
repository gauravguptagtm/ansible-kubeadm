node
=======

This role runs `kubeadm join` command in slave node which we store in master node. It is used for join slave node to kubernetes cluster.

Role Variables
--------------

We need to mention the path of join script which we run in slave node. For this, defined variable is(see `defaults/main.yml`):

    dest_path: ""

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: slave
      roles:
         - { role: node, dest_path: "/tmp/join_url.sh" }


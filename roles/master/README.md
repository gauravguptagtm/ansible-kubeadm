master
=========

Role for Kubernetes master node setup

Role Variables
--------------

Available variables are listed below, along with default values(see `defaults/main.yml`): 

    init_args: ""

If you need to mention some extra arguments in kubeadm init command, then mention it in init_args variable. 

To join master node, we need to run the `kubeadm join` command. To store this command in a file, we need to metion the destination path.

    dest_path: "/tmp/join_url.sh"

To mention POD_NETWORK_CIDR, we need to set variable...

    pod_network_cidr: 10.244.0.0/16

In INIT command, we also need to mention IP of cluster `--control-plane-endpoint`, for that we give variables...

    master_ip: "{{ hostvars[inventory_hostname][\"inventory_hostname\"] }}"


Dependencies
------------

None.

Example Playbook
----------------

    - hosts: master
      roles:
         - { role: master }


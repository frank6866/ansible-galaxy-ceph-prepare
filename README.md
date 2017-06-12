# Prepare for Ceph Deployment

This role is used to do some prepare work before deploy ceph, including the following:

* configure ntp if you do configur
* disable firewall
* create user for ceph-deploy


Role Variables
--------------
```
ceph_prepare_install_ntp: "true"

ip_hostname_in_etc_hosts:
  - ip: 192.168.10.11
    hostname: frank6866-1
    state: present
  - ip: 192.168.10.12
    hostname: frank6866-2
    state: present

ceph_prepare_user:
  - name: frank6866
    public_key: ssh-rsa xxx
```

Example Playbook
----------------

```
- hosts: ceph-prepare
  become: true
  roles:
    - frank6866.ceph-prepare
```

License
-------

MIT


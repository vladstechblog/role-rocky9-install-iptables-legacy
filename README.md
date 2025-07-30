role-rocky9-install-iptables-legacy
=========

Installs iptables-legacy, ebtables-legacy, and dependencies

This role already provides and EPEL9 repo GPG [key](files/RPM-GPG-KEY-EPEL-9)

Requirements
------------

- requuired EPEL9 rpm packages are pre-downloade and stored
  on the Ansible controller

Role Variables
--------------

- `rpm_src_dir`: local directory whre EPEL9 GPG key and RPMs live

- `rpm_package_list`: list of RPM packages to be installed
  see [vars](vars/Rocky_9.yml)

- `epel9_tmp_dir`: temporary directory where RPM package will be stored
  on the remote host (will be deleted). 

Dependencies
------------

N/A

Example Playbook
----------------


```yaml
- hosts: servers
  become: true

  roles:
     - role: role-rocky9-install-iptables-legacy
       rpm_src_dir: "{{ playbook_dir}}/common_files/epel9 }}"
```


License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

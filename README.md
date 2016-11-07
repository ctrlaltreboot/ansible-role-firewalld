ansible-role-firewalld
======================

Currently only tested and compatible with CentOS 7.
Starts and enables firewalld.
Configures allowed services via a hash variable.

Role Variables
--------------

This is a basic role that manages lets you open up popular service ports
on firewalld.

The default variable is like so:

```
firewalld_services:
  ssh:
    zone: public
    state: enabled
  http:
    zone: public
    state: enabled
  https:
    zone: public
    state: enabled
```

This opens up http, https and ssh.

Dependencies
------------

None

Example Playbook
----------------

```
- hosts: servers
  roles:
     - { role: xyzrbt.firewalld }
```

License
-------

GPLv2

Author Information
------------------

github.com/xyzrbt

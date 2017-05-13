Ansible Role: Install Python on newly bootstrapped Ubuntu host
=========

**Install Python on newly bootstrapped Ubuntu host**

This Ansible role will install Python on newly bootstrapped host. This is usually
a new host which you never even SSH-ed to.

In order for Ansible to work, Python must be installed (if missing).

Requirements
------------

None.

Role Variables
--------------

Comment `enable_fact_gather` variable if you don't want to gather facts
after this task has been executed (see: `defaults/main.yml`)

```
enable_fact_gather: "- setup: # aka gather_facts: yes"
```

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  remote_user: ubuntu # optional
  become: yes

  pre_tasks:
  roles: [ AdnanHodzic.python-ubuntu-bootstrap ]

  roles:
    ...
```

License
-------

GPLv3

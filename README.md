Ansible Role: Docker and Docker Compose setup
=========

**Install and Setup Docker and Docker Compose on any Ubuntu Linux system.**

This Ansible role will perform all necessary tasks to setup and run Docker and Docker Compose:

  * Install packages necessary for APT to use a repository over HTTPS.
  * Add and setup official Docker APT repositories.
  * Install packages needed for AUFS storage drivers.
  * Add user to Docker group.
  
This role was created as part of [containerized-wordpress-project](https://github.com/AdnanHodzic/containerized-wordpress-project)

Requirements
------------

None.

Role Variables
--------------

If you want to change user which will be added to Docker group
change contents of `system_user` variable (see: `defaults/main.yml`)

```
system_user: docker
```

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  remote_user: "{{ system_user }}"
  gather_facts: yes
  become: yes

  roles:
    - { role: AdnanHodzic.docker-compose }
```

License
-------

GPLv3

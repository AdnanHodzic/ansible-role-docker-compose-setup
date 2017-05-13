Role Name
=========

Install Docker and Docker Compose any Ubuntu Linux system.

Perform all necessary tasks to setup and run Docker and Docker Compose:

  * Install packages necessary for APT to use a repository over HTTPS.
  * Add and setup official Docker APT repositories.
  * Install packages needed for AUFS storage drivers.
  * Add user to Docker group.

Requirements
------------

None.

Role Variables
--------------

If you want to change user which will be added to Docker group
change contents of system_user variable (defaults/main.yml)

system_user: ubuntu

Dependencies
------------

None.

Example Playbook
----------------

- hosts: servers
  roles:
    - { role:  AdnanHodzic.docker-compose }

License
-------

GPLv3

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

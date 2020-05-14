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


Donate
-------

Since I'm working on this project in free time, please consider supporting this project by making a donation of any amount!

##### PayPal
[![paypal](https://www.paypalobjects.com/en_US/NL/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=7AHCP5PU95S4Y&item_name=Contribution+for+work+on+containerized-wordpress-project&currency_code=EUR&source=url)

##### BitCoin
[bc1qlncmgdjyqy8pe4gad4k2s6xtyr8f2r3ehrnl87](bitcoin:bc1qlncmgdjyqy8pe4gad4k2s6xtyr8f2r3ehrnl87)

[![bitcoin](https://foolcontrol.org/wp-content/uploads/2019/08/btc-donate-displaylink-debian.png)](bitcoin:bc1qlncmgdjyqy8pe4gad4k2s6xtyr8f2r3ehrnl87)

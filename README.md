supervisord-preconfig
=================

![Build Status](https://travis-ci.org/traveloka/ansible-supervisord-preconfig.svg?branch=master)

This roles is intended to configure some supervisord behaviours needed before deploying applications' supervisor configuration

Requirements
------------

This role does not install supervisord, you may want to install it with your package manager or pypi.

Dependencies
------------

None

Example Playbook
----------------

```
---
- hosts: all
  become: true
  roles:
    - role: ansible-supervisord-preconfig
      supervisord_app_log_directories:
        - /opt/traveloka/log
    - role: ansible-supervisord-preconfig
      supervisord_service_disable: false

```

License
-------

MIT

Author Information
------------------

[Salvian Reynaldi](https://github.com/salvianreynaldi/)


==========
ROLE REDIS
==========

.. image:: https://img.shields.io/github/license/adfinis-sygroup/ansible-role-redis.svg?style=flat-square
  :target: https://github.com/adfinis-sygroup/ansible-role-redis/blob/master/LICENSE

.. image:: https://img.shields.io/travis/adfinis-sygroup/ansible-role-redis.svg?style=flat-square
  :target: https://travis-ci.org/adfinis-sygroup/ansible-role-redis

.. image:: https://img.shields.io/badge/galaxy-adfinis--sygroup.redis-660198.svg?style=flat-square
  :target: https://galaxy.ansible.com/adfinis-sygroup/redis

This role installs Redis, an in-memory data store.


Requirements
=============

none to date


Role Variables
===============

* redis_packages: redis installation package
* redis_service: service name
* redis_port: service port
* redis_interface: bind interface for redis connections
* redis_interface_fact_var: ansible fact variable for the redis_interface
* redis_pidfile: absolute path to pid file
* redis_log_level: log level, any of debug, verbose, notice, warning
* redis_logfile: absolute path to log file, empty string to log to stdout
* redis_password: brute-force safe password, < 512 chars
* redis_slave_of: replication master ip
* redis_slave_of_port: change port connection to master node
* redis_save_thresholds: list of snapshotting thresholds
* redis_db_dir: db will be written inside this directory
* redis_db_filename: filename of db dump

Dependencies
=============

none to date


Example Playbook
=================

.. code-block:: yaml

  - hosts: servers
    roles:
       - { role: adfinis-sygroup.redis }


License
========

`GPL-3.0 <https://github.com/adfinis-sygroup/ansible-role-redis/blob/master/LICENSE>`_


Author Information
===================

redis role was written by:

* Adfinis SyGroup AG | `Website <https://www.adfinis-sygroup.ch/>`_ | `Twitter <https://twitter.com/adfinissygroup>`_ | `GitHub <https://github.com/adfinis-sygroup>`_

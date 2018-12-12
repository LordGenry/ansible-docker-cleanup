Role Name
=========

[![Build Status](https://travis-ci.org/matic-insurance/ansible-docker-cleanup.svg?branch=master)](https://travis-ci.org/matic-insurance/ansible-docker-cleanup)

Remove docker images created before given timestamp.

Requirements
------------

This role tested on Ubuntu 14/16 but should be compatible with others.

Role Variables
--------------

You need to provide:

* `images_keep_time`: filter can be Unix timestamps, date formatted timestamps, or Go duration strings (e.g. `10,`, `1h30m`, `2018-01-02`,`2018-01-02T15:04:05`)

Dependencies
------------

* Docker version 1.13+

Example Playbook
----------------

    - role: matic-insurance.ansible_docker_cleanup
      images_keep_time: '24h'
      tags: ['docker']

License
-------

MIT

Author Information
------------------

Matic is a communication platform that connects lenders and borrowers originating a new home loan. A borrower now knows where they are in the loan process and what they need to do to complete the loan.
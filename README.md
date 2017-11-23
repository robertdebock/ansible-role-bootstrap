ansible-role-bootstrap
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-bootstrap.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-bootstrap)

Bootstrap a system (many flavors) to use Ansible, likely the first role to depend on.

Requirements
------------

Access to a repository containing packages, likely on the internet.
Ansible 2.3 or higher.

Role Variables
--------------

None known.

Dependencies
------------

None known. This is likely the role that comes first when using Ansible, many others will depend on this role.

Example Playbook
----------------

```
---
- hosts: all
  become: yes
  gather_facts: no

  roles:
    - robertdebock.ansible-role-bootstrap

  tasks:
    - name: do something.
      ping:
```

Fact gathering will be done in the role when all required software is installed.

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>

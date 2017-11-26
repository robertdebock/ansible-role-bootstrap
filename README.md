ansible-role-bootstrap
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-bootstrap.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-bootstrap)

Bootstrap a system (many flavors) to use Ansible, likely the first role to depend on. This role does not depend on other roles, but many others may depend on this role.

Requirements
------------

Access to a repository containing packages, likely on the internet.
Ansible 2.2 or higher.

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
- name: bootstrap
  hosts: all
  gather_facts: no
  become: yes

  roles:
    - ansible-role-bootstrap

  tasks:
    - name: test connnection
      ping:
```

Non-standard options:
- gather_facts is set to no, because machines may not have all required software installed to be able to use common Ansible mechanisms. This role does eventually run "setup", providing all facts, when the required software is installed.
- become is set to "yes". The first part of the playbook logs in as "remoteuser" (set in defaults/main.yml) and installs required software. After that, the user specified in your inventory or ansible.cfg is used.

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>

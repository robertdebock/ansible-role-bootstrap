bootstrap
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-bootstrap.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-bootstrap)

Bootstrap a system (many distributions) to use Ansible, likely the first role to depend on. This role does not depend on other roles, but many others may depend on this role.
This role installs required software to be able to run all ansible packaged modules.

The purpose of this role is to install all required software to be able to use all modules that come with Ansible.

A benefit is that this role prepares nearly any (Linux) system, including:
- Alpine
- ArchLinux
- CentOS
- Debian
- Fedora
- Red Hat
- OpenSUSE
- Ubuntu

Requirements
------------

- Access to a repository containing packages, likely on the internet.
- Ansible 2.2 or higher.

Role Variables
--------------

- bootstrap_user: The user to connect to initially when installing the required software. Because sudo may not be installed, a user that has permission to use the package manager of the operating system you're running this role against will be used to connect to the machine. The default (set in defaults/main.yml) is set to "root". When the required software is installed, this user is not used anymore.
- bootstrap_preview: Should extra software be installed to support all modules
in the "preview" state? This can be set to either "yes", "no" or unset. The
default (set in defaults/main.yml) is set to "yes".

Dependencies
------------

None known. This is likely the role that comes first when using Ansible, many other roles can depend on this role.

Example Playbook
----------------

```
---
- name: bootstrap
  hosts: all
  gather_facts: no
  become: yes

  roles:
    - robertdebock.bootstrap
      bootstrap_user: vagrant

  tasks:
    - name: test connection
      ping:
```

To install this role:
- Install this role individually using `ansible-galaxy install robertdebock.bootstrap`
- Use another role that depends on this one and run `ansible-galaxy install --role-file requirements.yml`:

```
---
- name: robertdebock.bootstrap
  src: robertdebock.bootstrap
```

Non-standard options:
- "gather_facts" is set to "no", because machines may not have all required software installed to be able to use common Ansible mechanisms. This role does run "setup" when python once installed, providing all facts, when the required software is installed.
- "become" is set to "yes". The first part of the playbook logs in as "remoteuser" (set in defaults/main.yml) and installs required software. After that, the user specified in your inventory or ansible.cfg is used.

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>

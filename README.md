bootstrap
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-bootstrap.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-bootstrap)

Bootstrap a system (many distributions) to be managed by Ansible, likely the first role to depend on. This role does not depend on other roles, but many others may depend on this role.

This role installs required software to be able to run all ansible packaged modules.

A benefit is that this role prepares nearly any (Linux) system, including:
- Alpine
- ArchLinux
- Busybox
- CentOS
- Debian
- Fedora
- Gentoo
- Red Hat
- OpenSUSE
- Ubuntu

[Unit tests](https://travis-ci.org/robertdebock/ansible-role-bootstrap) are done on every commit and periodically.

If you find issues, please register them in [GitHub](https://github.com/robertdebock/ansible-role-bootstrap/issues)

To test this role locally please use [Molecule](https://github.com/metacloud/molecule):
```
pip install molecule
molecule test --scenario-name fedora-latest
```
There are many scenarios available, please have a look in the `molecule/` directory.

Context
--------
This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/drawings/artifacts/bootstrap.png "Dependency")

Requirements
------------

- Access to a repository containing packages, likely on the internet.
- A recent version of Ansible. (Tests run on the last 3 release of Ansible.)

Role Variables
--------------

- bootstrap_user: The user to connect to initially when installing the required software. Because sudo may not be installed, a user that has permission to use the package manager of the operating system you're running this role against will be used to connect to the machine. When the required software is installed, this user is not used anymore. [default: `root`]
- bootstrap_preview: Should extra software be installed to support all modules in the "preview" state? Either `yes`, `no` or unset. [default: `yes`]
- bootstrap_wait_for_host: Should the bootstrap role wait for the host to be available. [default: `no`]
- bootstrap_package_state: If you would like packages to be updated, set this to `latest`. [default: `present`]

Dependencies
------------

None known. This is likely the role that comes first when using Ansible, many other roles can depend on this role.

Compatibility
-------------

This role has been tested against the following distributions and Ansible version:

|distribution|ansible 2.4|ansible 2.5|ansible 2.6|ansible-2.7|ansible-devel|
|------------|-----------|-----------|-----------|-----------|-------------|
|alpine-edge*|yes|yes|yes|yes|yes*|
|alpine-latest|yes|yes|yes|yes|yes*|
|archlinux|yes|yes|yes|yes|yes*|
|centos-6|yes|yes|yes|yes|yes*|
|centos-latest|yes|yes|yes|yes|yes*|
|debian-latest|yes|yes|yes|yes|yes*|
|debian-stable|yes|yes|yes|yes|yes*|
|debian-unstable*|yes|yes|yes|yes|yes*|
|fedora-latest|yes|yes|yes|yes|yes*|
|fedora-rawhide*|yes|yes|yes|yes|yes*|
|gentoo|yes|yes|yes|yes|yes*|
|opensuse-leap|yes|yes|yes|yes|yes*|
|opensuse-tumbleweed|yes|yes|yes|yes|yes*|
|ubuntu-artful|yes|yes|yes|yes|yes*|
|ubuntu-devel*|yes|yes|yes|yes|yes*|
|ubuntu-latest|yes|yes|yes|yes|yes*|

The star means the build may fail, it's marked as an experimental build.

Example Playbook
----------------

```
---
- name: bootstrap
  hosts: all
  gather_facts: no
  become: yes

  roles:
    - role: robertdebock.bootstrap
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
```

Non-standard options:
- "gather_facts" is set to "no", because machines may not have all required software installed to be able to use common Ansible mechanisms. This role does run "setup" when python once installed, providing all facts, when the required software is installed.
- "become" is set to "yes". The first part of the playbook logs in as "remoteuser" (set in defaults/main.yml) and installs required software. After that, the user specified in your inventory or ansible.cfg is used.

License
-------

Apache License, Version 2.0

Author Information
------------------

[Robert de Bock](https://robertdebock.nl/) <robert@meinit.nl>

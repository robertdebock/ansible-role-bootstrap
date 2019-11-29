Ansible Role: Bootstrap
=======================

[![Build Status](https://img.shields.io/travis/rembik/ansible-role-bootstrap/master.svg?logo=travis-ci&logoColor=EEE)][travis_ci]
[![GitHub release](https://img.shields.io/github/release/rembik/ansible-role-bootstrap.svg?&colorB=56b4b6&logo=github&logoColor=EEE)](https://github.com/rembik/ansible-role-bootstrap/releases)
[![Ansible Role](https://img.shields.io/ansible/role/36340.svg?colorB=56b4b6&logo=ansible&logoColor=EEE)][ansible_galaxy]
[![Ansible Role downloads](https://img.shields.io/ansible/role/d/36340.svg?label=downloads&logo=ansible&logoColor=EEE)][ansible_galaxy]

Prepare your system to be managed by Ansible.

Requirements
------------

- Access to repositories containing system packages, likely on the internet.
- A recent Ansible version (tested last 2 stable major versions).

Role Variables
--------------

These defaults are set in `defaults/main.yml`:

```yaml
---
# defaults file for bootstrap

# The user to use to connect to machines.
bootstrap_user: root

# Do you want to wait for the host to be available?
bootstrap_wait_for_host: no

# The number of seconds you want to wait during connection test before failing.
bootstrap_timeout: 3

# The number of retries during installation
bootstrap_retries: 3
```

Dependencies
------------

None.

Example Playbook
----------------

This example is taken from `molecule/playbook.yml`:
```yaml
---
- hosts: all
  gather_facts: no
  become: yes

  roles:
    - role: rembik.bootstrap
```

Role Tests
----------

[![Python](https://img.shields.io/badge/python-3.7-1488C6.svg)](https://www.python.org/)
[![Ansible](https://img.shields.io/badge/Ansible-2.8%20%7C%202.9%20%7C%20devel%2A-56b4b6.svg)](https://ansible.com/)

This role is tested periodically against the following Linux distributions:

|| [![Ansible](https://img.shields.io/badge/2.8-56b4b6.svg)](https://docs.ansible.com/ansible/2.8/) | [![Ansible](https://img.shields.io/badge/2.9-56b4b6.svg)](https://docs.ansible.com/ansible/2.9/)| [![Ansible](https://img.shields.io/badge/devel%2A-56b4b6.svg)](https://docs.ansible.com/ansible/devel/) |
|---|---|---|---|---|
| [![DockerDistro](https://img.shields.io/badge/Alpine-latest%20%7C%20edge%2A-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/alpine) | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] |
| [![DockerDistro](https://img.shields.io/badge/AmazonLinux-latest-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/amazonlinux) | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] |
| [![DockerDistro](https://img.shields.io/badge/ArchLinux-latest-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/r/archlinux/base) | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] |
| [![DockerDistro](https://img.shields.io/badge/CentOS-latest-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/centos) | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] |
| [![DockerDistro](https://img.shields.io/badge/Debian-latest%20%7C%20unstable%2A-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/debian) | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] |
| [![DockerDistro](https://img.shields.io/badge/Fedora-latest%20%7C%20rawhide%2A-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/fedora) | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] |
| [![DockerDistro](https://img.shields.io/badge/Gentoo-latest-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/r/gentoo/stage3-amd64) | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] |
| [![DockerDistro](https://img.shields.io/badge/Kali-latest-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/r/kalilinux/kali-linux-docker) | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] |
| [![DockerDistro](https://img.shields.io/badge/openSUSE-Leap%20%7C%20Tumbleweed-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/opensuse) | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] |
| [![DockerDistro](https://img.shields.io/badge/RedHat-latest-1488C6.svg?logo=docker&logoColor=EEE)](https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8/ubi) | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] |
| [![DockerDistro](https://img.shields.io/badge/Ubuntu-latest%20%7C%20devel%2A-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/ubuntu) | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] | [![Check](https://img.shields.io/badge/X-grey.svg)][travis_ci] |

> Asteriks means the build is allowed to fail, it's marked as an experimental build.

Contributing
------------

If you find issues, please register them at this [GitHub project issue page](https://github.com/rembik/ansible-role-bootstrap/issues/new/choose) or consider contributing code by following this [guideline](http://github.com/rembik/ansible-role-bootstrap/tree/master/.github/CONTRIBUTING.md).

License
-------

[Apache License, Version 2.0](https://github.com/rembik/ansible-role-bootstrap/blob/master/LICENSE)

Author Information
------------------

- [Robert de Bock](https://robertdebock.nl/) <robert@meinit.nl>
- [Brian Rimek](https://github.com/rembik)

[travis_ci]: https://travis-ci.org/rembik/ansible-role-bootstrap
[ansible_galaxy]: https://galaxy.ansible.com/rembik/bootstrap

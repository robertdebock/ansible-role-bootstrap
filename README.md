Ansible Role: Bootstrap
=======================

[![Build Status](https://img.shields.io/travis/rembik/ansible-role-bootstrap/master.svg?logo=travis&logoColor=EEE)](https://travis-ci.org/rembik/ansible-role-bootstrap)
[![GitHub release](https://img.shields.io/github/release/rembik/ansible-role-bootstrap.svg?&colorB=56b4b6&logo=github&logoColor=EEE)](https://github.com/rembik/ansible-role-bootstrap/releases)
[![Ansible Role](https://img.shields.io/ansible/role/36340.svg?colorB=56b4b6&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAEdUlEQVRYR61Xa4iUVRh+n8PMCjXOzHlPmZUlZlgpoVBBUdBlUyExTRJsyUrqdxcw6EKhBEUX6fKvG5l0IUvZUKSr1I8uZpCUCVLE0lZo6znn29mVcpv53jjTzDLOzux3Vvv+fs/znOf7zvO+7zmgE3hE5NQkSU4HcBoAJSJHSqXSEICRqcohllCpVObVarVb0jTtAzCvE09EDgPYLSKfAniPmYez9DMNeO+vTdP0QQCLs8Ta3h8hoke01i8BSLtxuxpwzpVEZDuA66a4cDv8u56enhsKhcKhTjodDXjvZ6dp+iGAC05y8TpdRH4noqXGmB/b9SYYsNbOIqJvAZzxfyze1BCRChFdYYw50Kp7nIGQbufcXgAXRS5eI6JfiWhOJH4wn89fMn369KEm/jgD1tqtAFZHihGAdeVyeYtz7msAl0XyvmDmqyYYSJLk0jRN90aKhH09xMxnh4Rba1cD2BrLJaJbmfnNgB//A9bajwFcHysC4FGt9WONkOWcc4MAZsbwReQPZj4PwLG6Ae/9QhHZF0NuYKq5XG5msVi03vs7tNabrbUbg6kpaNT/Qt2Ac+4JInpgCuS3mbnPe3+NiLzGzHNGR0dnjo2NhXJTkTrvMPOapoGQ5HMiiWH/rzTGfGmt3QzgdgA3aa37rbXbAKyK1BnWWht478si4iNJYfEDxpgFbbz3mXllkiS9aZp+EquVy+UuhLV2AYD9sSQRucsY86r3/l4ReXa8nIA5WusB59xPRHR+jJ5SqhdJkixO0/SjGELoZsw8I6TXe79SRDYTUalRCRuNMRu89/eIyHMxekS0NhhYEvp+DAHAJq31+ibWe7+oYWIhEQ2EMFpriwD+JKJpWZr1/DjnLiai77PA/80UmW2MGXTOvaCU6i+Xy7sbWQh/YkUzjN77l8NWZWkqpZaiUqmYarUaZnfWs4uZlzXwodzyYd4z8+OBaK3dAGBRCGNsrgK+WYa/RAyUZcy8yzl3PxE91eJ2p9Z6DYCjoS8Q0T6tdWKt/QrA5ZN81ZjWmusGrLXPA7h7EvCg1np2o2sOENG5rVgROZjP51cUi8WDLflYKyJbJtHcwcw31g1kVYKIrDfGbLLWLgXwQSdRETmqlLpNa729URXTvPdhq0wnPIDQwl+vGxCREMb9AOZ3AB8TkRnGmIpzrj+ELSMsT2qtH2pMyVcA3NkBb7XWswD8PT4NvfdXi8hnHcA/i0gYnQrAw5G9fgeA7SKyiYi4XRPAfVrreq9oP5C8C+DmrHI4mfci8hszzwUwNsGAiBScc3u6bMXJrFvnishfoTKYebzvdDqUhqn4TezhYoquljPzzlZO12N5uN0Q0dwpLtAN/g8RrWsewzINBMDw8DDXarVtRBSaywk/IjKilFqutf68YzlmKTvn+kTkGQBnZmFb34vIqFLqxXw+/3ShUDjcjZt5N2yE5xTv/SoR6SWiJQDO6iYoInuUUm8ppd4olUouy3SUgXaRkZGRGdVqdb6IhAtMGL9DIhKu5z+EQ0nWoq3v/wWf4hm52dSUyAAAAABJRU5ErkJggg==)](https://galaxy.ansible.com/rembik/bootstrap)
[![Ansible Role downloads](https://img.shields.io/ansible/role/d/36340.svg?label=downloads&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAEdUlEQVRYR61Xa4iUVRh+n8PMCjXOzHlPmZUlZlgpoVBBUdBlUyExTRJsyUrqdxcw6EKhBEUX6fKvG5l0IUvZUKSr1I8uZpCUCVLE0lZo6znn29mVcpv53jjTzDLOzux3Vvv+fs/znOf7zvO+7zmgE3hE5NQkSU4HcBoAJSJHSqXSEICRqcohllCpVObVarVb0jTtAzCvE09EDgPYLSKfAniPmYez9DMNeO+vTdP0QQCLs8Ta3h8hoke01i8BSLtxuxpwzpVEZDuA66a4cDv8u56enhsKhcKhTjodDXjvZ6dp+iGAC05y8TpdRH4noqXGmB/b9SYYsNbOIqJvAZzxfyze1BCRChFdYYw50Kp7nIGQbufcXgAXRS5eI6JfiWhOJH4wn89fMn369KEm/jgD1tqtAFZHihGAdeVyeYtz7msAl0XyvmDmqyYYSJLk0jRN90aKhH09xMxnh4Rba1cD2BrLJaJbmfnNgB//A9bajwFcHysC4FGt9WONkOWcc4MAZsbwReQPZj4PwLG6Ae/9QhHZF0NuYKq5XG5msVi03vs7tNabrbUbg6kpaNT/Qt2Ac+4JInpgCuS3mbnPe3+NiLzGzHNGR0dnjo2NhXJTkTrvMPOapoGQ5HMiiWH/rzTGfGmt3QzgdgA3aa37rbXbAKyK1BnWWht478si4iNJYfEDxpgFbbz3mXllkiS9aZp+EquVy+UuhLV2AYD9sSQRucsY86r3/l4ReXa8nIA5WusB59xPRHR+jJ5SqhdJkixO0/SjGELoZsw8I6TXe79SRDYTUalRCRuNMRu89/eIyHMxekS0NhhYEvp+DAHAJq31+ibWe7+oYWIhEQ2EMFpriwD+JKJpWZr1/DjnLiai77PA/80UmW2MGXTOvaCU6i+Xy7sbWQh/YkUzjN77l8NWZWkqpZaiUqmYarUaZnfWs4uZlzXwodzyYd4z8+OBaK3dAGBRCGNsrgK+WYa/RAyUZcy8yzl3PxE91eJ2p9Z6DYCjoS8Q0T6tdWKt/QrA5ZN81ZjWmusGrLXPA7h7EvCg1np2o2sOENG5rVgROZjP51cUi8WDLflYKyJbJtHcwcw31g1kVYKIrDfGbLLWLgXwQSdRETmqlLpNa729URXTvPdhq0wnPIDQwl+vGxCREMb9AOZ3AB8TkRnGmIpzrj+ELSMsT2qtH2pMyVcA3NkBb7XWswD8PT4NvfdXi8hnHcA/i0gYnQrAw5G9fgeA7SKyiYi4XRPAfVrreq9oP5C8C+DmrHI4mfci8hszzwUwNsGAiBScc3u6bMXJrFvnishfoTKYebzvdDqUhqn4TezhYoquljPzzlZO12N5uN0Q0dwpLtAN/g8RrWsewzINBMDw8DDXarVtRBSaywk/IjKilFqutf68YzlmKTvn+kTkGQBnZmFb34vIqFLqxXw+/3ShUDjcjZt5N2yE5xTv/SoR6SWiJQDO6iYoInuUUm8ppd4olUouy3SUgXaRkZGRGdVqdb6IhAtMGL9DIhKu5z+EQ0nWoq3v/wWf4hm52dSUyAAAAABJRU5ErkJggg==)](https://galaxy.ansible.com/rembik/bootstrap)

Prepare your system to be managed by Ansible.

Requirements
------------

- Access to repositories containing system packages, likely on the internet.
- A recent Ansible version (tested last 3 major versions).

Role Variables
--------------

These defaults are set in `defaults/main.yml`:

```yaml
---
# defaults file for bootstrap

# The user to use to connect to machines.
bootstrap_user: root

# Installed software to support modules flagged as "preview" (i.e. mysql_db).
# "yes", "no" or unset are valid.
bootstrap_preview: yes

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

[![Python](https://img.shields.io/badge/python-2.7%20%7C%203.6-1488C6.svg)](https://www.python.org/)

This role is tested periodically against the following Linux distributions and Ansible versions:

| [![Ansible](https://img.shields.io/badge/Ansible-grey.svg?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAEdUlEQVRYR61Xa4iUVRh+n8PMCjXOzHlPmZUlZlgpoVBBUdBlUyExTRJsyUrqdxcw6EKhBEUX6fKvG5l0IUvZUKSr1I8uZpCUCVLE0lZo6znn29mVcpv53jjTzDLOzux3Vvv+fs/znOf7zvO+7zmgE3hE5NQkSU4HcBoAJSJHSqXSEICRqcohllCpVObVarVb0jTtAzCvE09EDgPYLSKfAniPmYez9DMNeO+vTdP0QQCLs8Ta3h8hoke01i8BSLtxuxpwzpVEZDuA66a4cDv8u56enhsKhcKhTjodDXjvZ6dp+iGAC05y8TpdRH4noqXGmB/b9SYYsNbOIqJvAZzxfyze1BCRChFdYYw50Kp7nIGQbufcXgAXRS5eI6JfiWhOJH4wn89fMn369KEm/jgD1tqtAFZHihGAdeVyeYtz7msAl0XyvmDmqyYYSJLk0jRN90aKhH09xMxnh4Rba1cD2BrLJaJbmfnNgB//A9bajwFcHysC4FGt9WONkOWcc4MAZsbwReQPZj4PwLG6Ae/9QhHZF0NuYKq5XG5msVi03vs7tNabrbUbg6kpaNT/Qt2Ac+4JInpgCuS3mbnPe3+NiLzGzHNGR0dnjo2NhXJTkTrvMPOapoGQ5HMiiWH/rzTGfGmt3QzgdgA3aa37rbXbAKyK1BnWWht478si4iNJYfEDxpgFbbz3mXllkiS9aZp+EquVy+UuhLV2AYD9sSQRucsY86r3/l4ReXa8nIA5WusB59xPRHR+jJ5SqhdJkixO0/SjGELoZsw8I6TXe79SRDYTUalRCRuNMRu89/eIyHMxekS0NhhYEvp+DAHAJq31+ibWe7+oYWIhEQ2EMFpriwD+JKJpWZr1/DjnLiai77PA/80UmW2MGXTOvaCU6i+Xy7sbWQh/YkUzjN77l8NWZWkqpZaiUqmYarUaZnfWs4uZlzXwodzyYd4z8+OBaK3dAGBRCGNsrgK+WYa/RAyUZcy8yzl3PxE91eJ2p9Z6DYCjoS8Q0T6tdWKt/QrA5ZN81ZjWmusGrLXPA7h7EvCg1np2o2sOENG5rVgROZjP51cUi8WDLflYKyJbJtHcwcw31g1kVYKIrDfGbLLWLgXwQSdRETmqlLpNa729URXTvPdhq0wnPIDQwl+vGxCREMb9AOZ3AB8TkRnGmIpzrj+ELSMsT2qtH2pMyVcA3NkBb7XWswD8PT4NvfdXi8hnHcA/i0gYnQrAw5G9fgeA7SKyiYi4XRPAfVrreq9oP5C8C+DmrHI4mfci8hszzwUwNsGAiBScc3u6bMXJrFvnishfoTKYebzvdDqUhqn4TezhYoquljPzzlZO12N5uN0Q0dwpLtAN/g8RrWsewzINBMDw8DDXarVtRBSaywk/IjKilFqutf68YzlmKTvn+kTkGQBnZmFb34vIqFLqxXw+/3ShUDjcjZt5N2yE5xTv/SoR6SWiJQDO6iYoInuUUm8ppd4olUouy3SUgXaRkZGRGdVqdb6IhAtMGL9DIhKu5z+EQ0nWoq3v/wWf4hm52dSUyAAAAABJRU5ErkJggg==)](https://ansible.com/) | [![Ansible](https://img.shields.io/badge/2.6-56b4b6.svg)](https://docs.ansible.com/ansible/2.6/) | [![Ansible](https://img.shields.io/badge/2.7-56b4b6.svg)](https://docs.ansible.com/ansible/2.7/) | [![Ansible](https://img.shields.io/badge/2.8-56b4b6.svg)](https://docs.ansible.com/ansible/2.8/)| [![Ansible](https://img.shields.io/badge/devel%2A-56b4b6.svg)](https://docs.ansible.com/ansible/devel/) |
|---|---|---|---|---|
| [![DockerDistro](https://img.shields.io/badge/Alpine-latest%20%7C%20edge%2A-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/alpine) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) |
| [![DockerDistro](https://img.shields.io/badge/ArchLinux-latest-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/r/archlinux/base) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) |
| [![DockerDistro](https://img.shields.io/badge/CentOS-latest-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/centos) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) |
| [![DockerDistro](https://img.shields.io/badge/Debian-latest%20%7C%20unstable%2A-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/debian) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) |
| [![DockerDistro](https://img.shields.io/badge/Fedora-latest%20%7C%20rawhide%2A-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/fedora) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) |
| [![DockerDistro](https://img.shields.io/badge/Gentoo-latest-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/r/gentoo/stage3-amd64) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) |
| [![DockerDistro](https://img.shields.io/badge/Kali-latest-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/r/kalilinux/kali-linux-docker) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) |
| [![DockerDistro](https://img.shields.io/badge/openSUSE-Leap%20%7C%20Tumbleweed-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/opensuse) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) |
| [![DockerDistro](https://img.shields.io/badge/Ubuntu-latest%20%7C%20devel%2A-1488C6.svg?logo=docker&logoColor=EEE)](https://hub.docker.com/_/ubuntu) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) | [![Check](https://img.shields.io/badge/X-grey.svg)](https://travis-ci.org/rembik/ansible-role-bootstrap) |

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

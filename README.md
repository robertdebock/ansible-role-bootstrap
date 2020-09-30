# [bootstrap](#bootstrap) - A Front-end Library

Prepare your system to be managed by Ansible.

|Travis|GitHub|Quality|Downloads|Version|
|------|------|-------|---------|-------|
|[![travis](https://travis-ci.com/robertdebock/ansible-role-bootstrap.svg?branch=master)](https://travis-ci.com/robertdebock/ansible-role-bootstrap)|[![github](https://github.com/robertdebock/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/robertdebock/ansible-role-bootstrap/actions)|[![quality](https://img.shields.io/ansible/quality/21642)](https://galaxy.ansible.com/robertdebock/bootstrap)|[![downloads](https://img.shields.io/ansible/role/d/21642)](https://galaxy.ansible.com/robertdebock/bootstrap)|[![Version](https://img.shields.io/github/release/robertdebock/ansible-role-bootstrap.svg)](https://github.com/robertdebock/ansible-role-bootstrap/releases/)|

## [Example Playbook](#example-playbook)

This example is taken from `molecule/resources/converge.yml` and is tested on each push, pull request and release.
```yaml
---
- name: Converge
  hosts: all
  become: yes
  gather_facts: no

  roles:
    - role: robertdebock.bootstrap
```

The machine may need to be prepared using `molecule/resources/prepare.yml`:
```yaml
No preparation required.
```

For verification `molecule/resources/verify.yml` runs after the role has been applied.
```yaml
---
- name: Verify
  hosts: all
  become: no
  gather_facts: no

  tasks:
    - name: test connection
      ping:
```

Also see a [full explanation and example](https://robertdebock.nl/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

These variables are set in `defaults/main.yml`:
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

## [Requirements](#requirements)

- Access to a repository containing packages, likely on the internet.
- A recent version of Ansible. (Tests run on the current, previous and next release of Ansible.)

The following roles can be installed to ensure all requirements are met, using `ansible-galaxy install -r requirements.yml`:

```yaml
- none
```

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/drawings/artifacts/bootstrap.png "Dependency")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/robertdebock):

|container|tags|
|---------|----|
|alpine|all|
|amazon|2018.03|
|el|7, 8|
|debian|buster, bullseye|
|fedora|31, 32|
|opensuse|all|
|ubuntu|focal, bionic, xenial|

The minimum version of Ansible required is 2.9, tests have been done to:

- The previous version.
- The current version.
- The development version.



## [Testing](#testing)

[Unit tests](https://travis-ci.com/robertdebock/ansible-role-bootstrap) are done on every commit, pull request, release and periodically.

If you find issues, please register them in [GitHub](https://github.com/robertdebock/ansible-role-bootstrap/issues)

Testing is done using [Tox](https://tox.readthedocs.io/en/latest/) and [Molecule](https://github.com/ansible/molecule):

[Tox](https://tox.readthedocs.io/en/latest/) tests multiple ansible versions.
[Molecule](https://github.com/ansible/molecule) tests multiple distributions.

To test using the defaults (any installed ansible version, namespace: `robertdebock`, image: `fedora`, tag: `latest`):

```
molecule test

# Or select a specific image:
image=ubuntu molecule test
# Or select a specific image and a specific tag:
image="debian" tag="stable" tox
```

Or you can test multiple versions of Ansible, and select images:
Tox allows multiple versions of Ansible to be tested. To run the default (namespace: `robertdebock`, image: `fedora`, tag: `latest`) tests:

```
tox

# To run CentOS (namespace: `robertdebock`, tag: `latest`)
image="centos" tox
# Or customize more:
image="debian" tag="stable" tox
```

## [License](#license)

Apache-2.0

## [Contributors](#contributors)

I'd like to thank everybody that made contributions to this repository. It motivates me, improves the code and is just fun to collaborate.

- [rembik](https://github.com/rembik)
- [jellevandehaterd](https://github.com/jellevandehaterd)
- [fzarifian](https://github.com/fzarifian)
- [kmonticolo](https://github.com/kmonticolo)
- [CrystalStiletto](https://github.com/CrystalStiletto)
- [infothrill](https://github.com/infothrill)

## [Author Information](#author-information)

[Robert de Bock](https://robertdebock.nl/)

Please consider [sponsoring me](https://github.com/sponsors/robertdebock).

# How to contribute

Thanks! There are a few guidelines that we need contributors to follow so that we can keep on top of things.

## Report

You can report bugs or make enhancement requests at this [GitHub project issue page](http://github.com/rembik/ansible-role-bootstrap/issues/new/choose) by filling out the issue template that will be presented.

## Develop

You are very welcome to develop bug fixes or features. Please make sure to run tests before making a [pull request](https://help.github.com/articles/creating-a-pull-request/) to this GitHub project.

## Test

This role uses [Molecule](https://github.com/metacloud/molecule) for testing and that, in turn, uses Ansible to deploy the needed test infrastructure:
```
sudo pip install ansible
sudo pip install molecule
```

You can decide, if you want to run the tests locally with Docker, Vagrant or on Amazon EC2. Follow the respective requirements for that:
- [Docker](http://github.com/rembik/ansible-role-bootstrap/tree/master/molecule/docker-all/INSTALL.rst)
- [Amazon EC2](http://github.com/rembik/ansible-role-bootstrap/tree/master/molecule/ec2-all/INSTALL.rst)
- [Vagrant](http://github.com/rembik/ansible-role-bootstrap/tree/master/molecule/vagrant/INSTALL.rst)

Then run the test with the chosen deployment method:
```
molecule test --senario-name default
molecule test --senario-name docker-all

molecule test --scenario-name ec2
molecule test --scenario-name ec2-all

molecule test --scenario-name vagrant
```

In addition, if you want to run the tests on different Ansible versions locally with Docker and/or on Amazon EC2, use [tox](https://tox.readthedocs.io/en/latest/):
```
sudo pip install tox-travis

tox
```

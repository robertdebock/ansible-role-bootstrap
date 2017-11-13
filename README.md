Bootstrap
=========

Bootstrap a system (many flavors) to use Ansible, likely the first role to depend on.

Requirements
------------

Access to a repository containing packages, likely on the internet.

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

  roles:
    - robertdebock.bootstrap

  tasks:
    - name: do something.
      ping:
```

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>

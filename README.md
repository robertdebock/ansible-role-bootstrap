Role Name
=========

Bootstrap a system to use Ansible.

Requirements
------------

None known.

Role Variables
--------------

None known.

Dependencies
------------

None know. This is likely the role that comes first when using ansible, many others will depend on this role.

Example Playbook
----------------

```
---
- hosts: servers
  become: yes
  roles:
    - bootstrap
```

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>

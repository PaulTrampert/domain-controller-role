Role Name
=========

Sets up a Samba4 based active directory domain controller.

Requirements
------------

Python3

Role Variables
--------------

- `hostname`: The hostname to use for the machine.
- `ad_realm`: The fully qualified realm for the domain (e.g. `some.sample.com`)
- `ad_domain`: The NETBios name for the domain (e.g. `SAMPLE`)
- `ad_admin_pass`: The password for the domain administrator.
- `ad_dc_ip`: The static IP address for the domain controller. Defaults to `ansible_default_ipv4.address`.

Example Playbook
----------------

```yml
---
- hosts: all
  become: yes
  vars:
    hostname: dc01
    ad_realm: home.ptrampert.com
    ad_domain: PTRAMPERT
    ad_admin_pass: Asdfasdf1
  roles:
    - domain-controller-role
```

License
-------

MIT

Author Information
------------------

https://github.com/PaulTrampert

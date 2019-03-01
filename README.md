Ansible Role - incron
=========
[![Build Status](https://travis-ci.org/jadbaz/ansible-role-incron.svg?branch=master)](https://travis-ci.org/jadbaz/ansible-role-incron)

(Forked from: [vkill/ansible-role-incron](https://github.com/vkill/ansible-role-incron))

Incron Installation.

Requirements
------------

None.

Role Variables
--------------

TODO

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers
  become: true

  roles:
    - role: jadbaz.incron
      incron_system_tables:
        - name: demo
          path: /home/
          mask: IN_CREATE,IN_DELETE
          command: /tmp/incron_demo.sh $# $%
```

[detailed example](vagrant_playbook.yml)

Local Testing with Vagrant
----------------

* Run vagrant

```shell
$ vagrant up --no-provision
$ vagrant provision
```

License
-------

MIT / BSD

Author Information
------------------

vkill <vkill.net@gmail.com>

&copy; 2016

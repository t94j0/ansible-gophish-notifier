Ansible - GoPhish Notifier
=========

[![t94j0.gophish_notifier](https://img.shields.io/ansible/role/55987)](https://galaxy.ansible.com/t94j0/gophish_notifier)

Install [GoPhish Notifier](https://github.com/t94j0/gophish-notifier)

Role Variables
--------------

`config` - Dictionary containing configuation

Dependencies
------------

None

Example Playbook
----------------

Configuration as YAML in `/etc/gophish_notifier/config.yml`.

```
- hosts: servers
  roles:
     - include_role:
         name: t94j0.gophish_notifier
       vars:
         config:
           secret: abc123
           base_url: https://localhost:3333
           profiles:
             - slack
           slack:
             webhook: 'https://hooks.slack.com/services/...'
             bot_channel: '#testing'
```


License
-------

MIT

Author Information
------------------

Max Harley

Caddy
=========
[![Galaxy](https://img.shields.io/badge/galaxy-samdoran.caddy-blue.svg?style=flat)](https://galaxy.ansible.com/samdoran/caddy)
[![Build Status](https://travis-ci.com/samdoran/ansible-role-caddy.svg?branch=master)](https://travis-ci.com/samdoran/ansible-role-caddy)

Install [Caddy](https://caddyserver.com) with a basic config set to include `conf.d/*.conf`. Roles that wish to use Caddy should place their config file in that directory with a `.conf` extension.

Requirements
------------

None.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `caddy_service_name` | `caddy` | Name of the service for starting/stopping/enabling. |
| `caddy_default_port` | `80` | Default port Caddy will bind to. |
| `caddy_config_path` | `/etc/caddy` | Path to Caddy config. |
| `caddy_config_file` | `caddy.conf` | Name of the Caddy config file. |
| `caddy_root` | `/usr/share/caddy` | Path to the default root served by Caddy. |
| `caddy_global_config_options` | `[]` | List of global Caddy config options. Syntax must be correct. |


Dependencies
------------

- `community.general` collection

Example Playbook
----------------

    - hosts: all
      roles:
         - samdoran.caddy

License
-------

Apache 2.0

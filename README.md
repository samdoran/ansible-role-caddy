Caddy
=========
[![Galaxy](https://img.shields.io/badge/galaxy-samdoran.caddy-blue.svg?style=flat)](https://galaxy.ansible.com/samdoran/caddy)
[![Build Status](https://travis-ci.org/samdoran/ansible-role-caddy.svg?branch=master)](https://travis-ci.org/samdoran/ansible-role-caddy)

Install [Caddy](https://caddyserver.com) with a basic config set to include `conf.d/*.conf`. Roles that wish to use Caddy should place their config file in that directory with a `.conf` extension.

Requirements
------------

None.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `caddy_user` | `caddy` | Caddy user. |
| `caddy_group` | `caddy` | Caddy group. |
| `caddy_service_name` | `caddy` | Name of the service for starting/stopping/enabling. |
| `caddy_default_port` | `80` | Default port Caddy will bind to. |
| `caddy_log_path` | `/var/log/caddy` | Path to Caddy logs. |
| `caddy_config_path` | `/etc/caddy` | Path to Caddy config. |
| `caddy_config_file` | `caddy.conf` | Name of the Caddy config file. |
| `caddy_root` | `/usr/share/caddy` | Path to the default root served by Caddy. |
| `caddy_force_update` | `false` | Whether or not to replace an existing `caddy` binary with a newly downloaded one. By default, if a a `caddy` binary exists, it will not be replaced. |
| `caddy_license_type` | `personal` | Caddy license type. More information [here](https://caddyserver.com/products/licenses) |
| `caddy_plugins` | `[see defauts/main.yml]` | List of Caddy options to add when building a custom Caddy binary. |


Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      roles:
         - samdoran.caddy

License
-------

Apache 2.0

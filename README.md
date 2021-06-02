# Ansible Auto Update

[![CI](https://github.com/akutschi/ansible_auto_update/actions/workflows/ci.yml/badge.svg)](https://github.com/akutschi/ansible_auto_update/actions/workflows/ci.yml)

This is a very simple role to update the whole OS.
On top of that unattended upgrades are configured and enabled. 
Unattended upgrades are in a way configured not that just security updates will be installed, but all possible updates will be installed when they are available.

## Requirements

This role does not have any requirements.

## Coverage

Any combination of the following is tested:

- Operating System
  - Ubuntu 20.04 LTS
  - Debian 10
- Ansible
  - 2.9.x
  - 3.x
  - 4.x 
- Python
  - 3.8
  - 3.9

## Install Role

To install this role into your `roles` folder just clone, download or run: 

```bash
ansible-galaxy install --roles-path ./roles git+https://github.com/akutschi/ansible_auto_update.git,v0.2.0
```

## Role Variables

Here you can see all settable variables for this role. The defaults can be found in `defaults/main.yml`. 
The defaults are chosen in a reasonable way, so that no additional parameters must be set to the role.

| Variable | Default | Description
|-|-|-|
| apt_auto_update_enable | `1` | Enables/disables automatic updates |
| apt_auto_update_list_schedule | `1` | `apt-get update` every `n` days |
| apt_auto_update_unattended_schedule | `1` | Run `unattended-upgrade` every `n` days |
| apt_auto_update_download_schedule | `1` | Download upgradeable packages every `n` days |
| apt_auto_update_clean_schedule | `21` | Clean up local cache every `n` days |

## Dependencies

This role does not have any dependencies.

## Example Playbook

```yml
---
- hosts: servers
  roles:
      - ansible_auto_update
```

# License

GPLv3, see [license](./LICENSE).

# Contributing

Feel free to open issues or merge requests if you find problems or have ideas for improvements. Thank you.

# Ansible Update

This is a very simple role to update the whole OS.
On top of that unattended upgrades are configured and enabled. 
Unattended upgrades are in a way configured not that just security updates will be installed, but all possible updates will be installed when they are available.

## Requirements

- This version requires Ubuntu 20.04 LTS
- Ansible 2.9.x, this role is **not tested with Ansible 2.10** yet.

## Role Variables

There are no settable variables in this role.

## Dependencies

This role does not have any dependencies.

## Example Playbook

The setup is quite simple.
Just clone or download this role into your `roles` folder and set up the playbook similar to this example:

```yml
---
- hosts: servers
  roles:
      - ansible-update
```

# License

GPLv3, see [license](./LICENSE).

# Contributing

Feel free to open issues or merge requests if you find problems or have ideas for improvements. Thank you.

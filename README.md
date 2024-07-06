# Ansible Role: Node Exporter

[![CI](https://github.com/DudeCalledBro/ansible-role-sudo/actions/workflows/molecule.yml/badge.svg)](https://github.com/DudeCalledBro/ansible-role-sudo/actions/workflows/molecule.yml)

Install and Configure Sudo on Linux Systems!

## Prerequisites

- Ensure you have Ansible installed (e.g. `pip3 install ansible`)

## Role Variables

The default values for the variables are set in [defaults/main.yml](./defaults/main.yml)

```yaml
sudo_sudoersd_path: /etc/sudoers.d
sudo_sudoersd_owner: root
sudo_sudoersd_group: root

# define sudoers files (ensure name and content)
sudo_sudoers_files: []
# - name: 10-ansible
#   content: |
#     {{ ansible_managed }}
#     ansible ALL=(ALL) NOPASSWD: ALL
```

```yaml
- hosts: all
  roles:
  - role: dudecalledbro.sudo
```

## License

Copyright © 2024 Niclas Spreng

Licensed under the [MIT license](LICENSE).

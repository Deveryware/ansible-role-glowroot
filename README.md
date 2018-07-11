# Ansible Role Glowroot

This Ansible role installs and configures Glowroot (Official website: https://glowroot.org/).

## Prerequisites

* None

## Usage

    http://localhost:4000

# Example Playbook

    - hosts: servers
      roles:
      - ansible-role-glowroot
        glowroot_bind_address: '0.0.0.0'

## License

MIT

## Author Information

This role was created in 2018 by Olivier Locard on the behalf of Deveryware.


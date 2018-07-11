# Ansible Role Glowroot

This Ansible role installs and configures Glowroot (Official website: https://glowroot.org/).

## Prerequisites

* None

## Usage

    http://localhost:4000

## Example Playbook

    - hosts: servers
      roles:
      - ansible-role-glowroot
        glowroot_bind_address: '0.0.0.0'

## Variables

    glowroot_port: 4000
    glowroot_bind_address: '127.0.0.1'
    glowroot_context_path: '/'

    glowroot_owner: 'root'
    glowroot_group: 'root'

## License

MIT

## Author Information

This role was created in 2018 by Olivier Locard on the behalf of Deveryware.


# Ansible Role Glowroot

This Ansible role installs and configures Glowroot (Official website: https://glowroot.org/).

## Prerequisites

* None

## Usage

    http://localhost:4000

Default credentials; admin / admin

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
    glowroot_group: 'glowroot'

    glowroot_group_members:
    - 'my_app_account'

### LDAP

    glowroot_ldap_host: 'ldap.company.eu'
    glowroot_ldap_port: 636
    glowroot_ldap_ssl: true
    glowroot_ldap_username: 'ldapviewer'
    glowroot_ldap_password: '005PQPXB31t5QEc+UZNRkw:Kzs7v+nDPl4bwkOWCFRrDw:500000'
    glowroot_user_base_dn: 'ou=User,dc=company,dc=eu'
    glowroot_user_search_filter: '(uid={0})'
    glowroot_group_base_dn: 'ou=Groups,dc=company,dc=eu'
    glowroot_group_search_filter: 'member={0}'

You will have to set the _password_ into the webui in order to retrieve the hash in the file `admin.json`.

### Storage

### data.h2.db

**Response time and JVM gauge data** respectively 1 minute, 5 minutes, 30 mintes and 4 hours aggregates:

    glowroot_rtjg_1m: 72
    glowroot_rtjg_5m: 336
    glowroot_rtjg_30m: 2160
    glowroot_rtjg_4h: 2160

    glowroot_trace_data: 336
    glowroot_full_query_text: 336

### .capped.db

**Query, service call and profile data** respectively 1 minute, 5 minutes, 30 mintes and 4 hours aggregates:

    glowroot_qscp_1m: 500
    glowroot_qscp_5m: 500
    glowroot_qscp_30m: 500
    glowroot_qscp_4h: 500

    glowroot_trace_detail_data: 500

## License

MIT

## Author Information

This role was created in 2018 by Olivier Locard on the behalf of Deveryware.


# Ansible Role: PM2 (NodeJS Process Manager)

Installs PM2 service on RHEL/CentOS (https://pm2.keymetrics.io/)

## Requirements

None.

## Role Variables

See `defaults/main.yml`

## Example Playbook

    - hosts: webnodes
      roles:
         - { role: classyllama.pm2, tags: pm2, when: use_classyllama_pm2 | default(false) }

## License

This work is licensed under the MIT license. See LICENSE file for details.

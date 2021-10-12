# Ansible Role: PM2 (NodeJS Process Manager)

Installs PM2 service on RHEL/CentOS (https://pm2.keymetrics.io/)

## Requirements

None.

## Role Variables

    pm2_app_name: pwa                  # Application name 
    pm2_service_name: pm2-data-pwa     # Systemd service name
    pm2_user: www-data-pwa             # Linux username for pm2 service
    pm2_user_home: /home/www-data-pwa  # Home directory for .pm2 configuration files and logs
    pm2_pool_dir: /var/www/data-pwa    # Root application folder
    pm2_platform: ""                   # Platform automatically detected when left blank (systemd for CentOS 7, 8)

## Example Playbook

    - hosts: webnodes
      roles:
         - { role: classyllama.pm2, tags: pm2, when: use_classyllama_pm2 | default(false) }

## License

This work is licensed under the MIT license. See LICENSE file for details.

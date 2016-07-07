# ansible-lemp
Ansible playbook for install LEMP stack

# Ansible playbook for install LEMP stack
1. Install Ansible [Install Ansible](http://docs.ansible.com/ansible/intro_installation.html)
2. Clone repository from Github `https://github.com/belaytzev/ansible-lemp.git`
3. Run playbook `ansible-playbook install_lemp.yml`

# Vars
```
    #Role common
    packages:
      - sudo
      - mc
      - atop
      - htop
      - rcconf
      - ncdu
      - git
      - ntp
      - cron
      - curl
      - locales
      - unattended-upgrades

    timezone: Europe/Moscow
    locales: ru_RU.UTF-8

    #Role Nginx
    nginx_server_name: example.com
    nginx_project_name: Example
    nginx_user: www-data
    nginx_root: "/var/www/{{ nginx_project_name }}"

    #Role PHP
    php_packages:
      - php5
      - php5-cli
      - php5-fpm
      - php5-curl
      - php5-gd
      - php5-json
      - php5-mcrypt

    php_time_zone: Europe/Moscow
    php_expose_php: Off
    php_short_open_tag: On

    #Role MySQL
    user_db: root
    passwd_db: root
```

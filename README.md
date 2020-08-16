# Ansible role: shiny
Web applications in R.

## DEPRECATED
Installation of this app has been moved to kubernetes,
so this ansible role is no longer maintained.

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `shiny_user` (default: shiny): unprivileged local user to run process under
+ `shiny_passwd`: login password
+ `shiny_host`: external virtual host for nginx
+ `shiny_localport` (default: 3838): nginx proxies to this
+ `shiny_listen` (default: [ localhost:80 ]): list of
  lines for 'listen' directive in nginx config

## Dependencies
+ R
+ nginx

## Example Playbook

```
- hosts: shiny
  roles:
    - { role: ho-ansible.shiny }
```

## License
MIT

## Author Information
Sean Ho, https://github.com/ho-ansible/

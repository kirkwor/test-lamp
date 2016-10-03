To Do:
 - PHPMyAdmin
 - Custom config for cached results
 - Custom FTP user
 - Restrict to sudo only

Completed:
 - Varnish server
 - Nginx server
 - PHP-FPM server
 - MariaDB server
 - FTP server server
 - Wordpress initial
 - Links between services

####

Temp usage pre-vagrant setup:

```bash
ansible-playbook site.yml
```
You can add -v at the end of it for a more detailed output.

Edit "hosts" entry in file site.yml from

```bash
- hosts: test
```
to
```bash
- hosts: your_host
```


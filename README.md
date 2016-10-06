####

To Do:
 - Restrict to sudo only
 - Custom config for cached results

Completed:
 - Varnish server
 - Nginx server
 - PHP-FPM server
 - MariaDB server
 - FTP server server
 - Wordpress initial
 - Links between services
 - phpMyAdmin
 - Custom FTP user

####

Requirements note:

Host should be using Centos 7.

Package python-passlib should be present on the host running ansible-playbook.

For phpmyadmin download, I've issued a git command instead of the classic "get zip, unzip" method that I've used for Wordpress.
This git method requries git version 1.9.1+ to use the "depth=1" option, this skips .git entire history to be downloaded i.e. use your disk space, if your git version is lower, then it will not fail (as it has a fallback method), but instead extra disk space will be used.

Your PC hosts file alteration for both WP and phpmyadmin URL should look like (if your server IP is 10.10.0.5):

```bash
10.10.0.5 www.test.com test.com pma.test.com
```

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


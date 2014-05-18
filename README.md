aspects_mysql_client
========

Ensure that the mysql command line client tools are installed. This does not install the server.

Requirements
------------

Set ```hash_behaviour=merge``` in your ansible.cfg file.

Role Variables
--------------

```yaml
aspects_mysql_client_package_name:
  Debian: "mysql-client"
  RedHat: "mysql"
```
Simply override the ```aspects_mysql_client_packge_name``` dictionary in your local vars files, if you need to change package names.

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - aspects_mysql_client

License
-------

MIT

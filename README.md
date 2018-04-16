# aspects_ntp_client

Manage which servers your server queries for ntp information, as well as a few other configuration options. This does **not** let you set up an ntp *server*.

## Requirements

Set ```hash_behaviour=merge``` in your ansible.cfg file.

## Role Variables

### aspects_ntp_client_enabled
Default: False

Set to ```True``` if you want the role tasks to run.

Set to ```False``` if you want to disable the role tasks.

### aspects_ntp_client_service_name
* Debian default: ntp
* RedHat default: ntpd
* Suse default: ntp

This variable is used to tell ansible what the service name is when handling the service. Values are set in the ```vars/{{ ansible_os_family }}.yml``` files.

## Example Playbook

TODO: Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }
```

## License

MIT

# aspects_ntp_client

Manage which servers your server queries for ntp information, as well as a few other configuration options. This does **not** let you set up an ntp *server*.

## Requirements

Set ```hash_behaviour=merge``` in your ansible.cfg file.

## Role Variables

### aspects_ntp_client_enabled
Default: False

Set to ```True``` if you want the role tasks to run.

Set to ```False``` if you want to disable the role tasks.

## Example Playbook

TODO: Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }
```

## License

MIT

# aspects_ntp_client

Manage which servers your server queries for ntp information, as well as a few other configuration options. This does **not** let you set up an ntp *server*.

## Requirements

Set ```hash_behaviour=merge``` in your ansible.cfg file.

## Role Variables

TODO: A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

## Example Playbook

TODO: Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }
```

## License

MIT

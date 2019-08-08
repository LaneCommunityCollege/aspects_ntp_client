# aspects_ntp_client

Manage which servers your server queries for ntp information, as well as a few other configuration options. This does **not** let you set up an ntp *server*.

## Requirements

Set ```hash_behaviour=merge``` in your ansible.cfg file.

## Role Variables

## aspects_packages_packages
Dictionary/hash of packages to install or remove. Uses the aspects_packages role.

### aspects_ntp_client_enabled
Default: False

Set to ```True``` if you want the role tasks to run.

Set to ```False``` if you want to disable the role tasks.

### aspects_ntp_client_service_name
`ntp` if `ansible_os_family` is "Debian". `ntpd` if `ansible_os_family` is "RedHat".

This variable is used to tell ansible what the service name is when handling the service.

## Dependencies
### aspects_packages
`aspects_packages` is used to install and remove OS packages.

## Example Playbook
On some systems, chrony is used by default instead of ntp. You can easily remove it just by adding a value to `aspects_packages_packages`. See the example below.

```yaml

- hosts:
  - aspects_ntp_client
  vars:
    aspects_ntp_client_enabled: True
    aspects_packages_enabled: True
    aspects_ntp_client_servers:
      - 0.ubuntu.pool.ntp.org
      - 1.ubuntu.pool.ntp.org
    aspects_packages_packages:
      chrony:
        state: "absent"
        Ubuntu:
          1604: "chrony"
          1804: "chrony"
        Debian:
          9: "chrony"
        CentOS:
          7: "chrony"
        OracleLinux:
          7: "chrony"
  roles:
  - aspects_ntp_client
```

## License

MIT

## nsclient

[NSClient++](https://https://www.nsclient.org//) role for Ansible

#### Variables

* `nsclient_settings_password`: [default: CHANGE_ON_INSTALL]: Password used to authenticate against server
* `nsclient_settings_allowed_hosts: [default: 127.0.0.1,::1]: A comaseparated list of allowed hosts. You can use netmasks (/ syntax) or * to create ranges..
* `nsclient_nrpe_ssloptions`: [default: None]: Comma separated list of verification flags to set on the SSL socket.
* `nsclient_nrpe_verify_mode`: [default: None]: Comma separated list of verification flags to set on the SSL socket.
* `nsclient_nrpe_insecure`: [default: false]: ALLOW INSECURE CHIPHERS and ENCRYPTION
* `nsclient_nrpe_allow_arguments`:  This option determines whether or not the we will allow clients to specify arguments to commands that are executed.
* `nsclient_nrpe_allow_nasty_chars`:  Allow potentially harmful characters in commands.
* `nsclient_modules_checkexternalscripts`: [default: 1]:
* `nsclient_modules_checkhelpers`: [default: 1]:
* `nsclient_modules_checkeventlog`: [default: 1]:
* `nsclient_modules_checknscp`: [default: 1]:
* `nsclient_modules_checkdisk`: [default: 1]:
* `nsclient_modules_checksystem`: [default: 1]:
* `nsclient_modules_nrpeserver`: [default: 1]:
* `nsclient_external_scripts_allow_arguments`
* `nsclient_external_scripts_allow_nasty_chars`
* `nsclient_external_scripts: []

## Dependencies

None

#### Basic installation

```yaml
---
- hosts: all
  roles:
    - janneojala.nsclient
  vars:
    nsclient_settings_password: CHANGE_ON_INSTALL
    nsclient_settings_allowed_hosts: 127.0.0.1,::1
    nsclient_external_scripts:
      - name: check_updates
        command: cmd /c echo scripts/check_windows_updates.ps1; exit $LastExitCode | powershell.exe -command -

```

#### License

MIT

#### Author Information

Janne Ojala

#### Issues

Are [welcome](https://github.com/janneojala/ansible-nsclient/issues)!

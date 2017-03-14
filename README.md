## nsclient

NSClient++ [NSClient](https://https://www.nsclient.org//) role for Ansible

#### Variables

* `nsclient_settings_password`: [default: CHANGE_ON_INSTALL]: PASSWORD - Password used to authenticate againast server
* `nsclient_settings_allowed_hosts: [default: 127.0.0.1,::1]: ALLOWED HOSTS - A comaseparated list of allowed hosts. You can use netmasks (/ syntax) or * to create ranges.
* `nsclient_nrpe_ssloptions`: [default:
* `nsclient_nrpe_verify_mode`: [default:
* `nsclient_nrpe_insecure`: [default: false]:
* `nsclient_nrpe_allow_arguments`: [default: true]: COMMAND ARGUMENT PROCESSING - This option determines whether or not the we will allow clients to specify arguments to commands that are executed.
* `nsclient_nrpe_verify_mode`: [default: none]:
* `nsclient_nrpe_insecure`: [default: true]:
* `nsclient_modules_checkexternalscripts`: [default: 1]:
* `nsclient_modules_checkhelpers`: [default: 1]:
* `nsclient_modules_checkeventlog`: [default: 1]:
* `nsclient_modules_checknscp`: [default: 1]:
* `nsclient_modules_checkdisk`: [default: 1]:
* `nsclient_modules_checksystem`: [default: 1]:
* `nsclient_modules_nrpeserver`: [default: 1]:
* `nsclient_external_scripts_allow_arguments`: [default: true]:
* `nsclient_external_scripts: []

## Dependencies

None

#### SSL Termination 1

* **Single core**
* Multiple certificates (SNI)
* Global monitoring
* Multiple web servers

```yaml
---
- hosts: all
  roles:
    - janneojala.ansible-nsclient
  vars:
    nsclient_settings_password: CHANGE_ON_INSTALL
	nsclient_settings_allowed_hosts: 127.0.0.1,::1

#### License

MIT

#### Author Information

Janne Ojala

#### Issues

Are [welcome](https://github.com/janneojala/ansible-nsclient/issues)!

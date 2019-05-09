process-exporter
================

Ansible role for install Prometheus exporter that mines /proc to report on selected processes.

Requirements
------------

Ansible

Role Variables
--------------

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `process_exporter_version` | 0.4.0 | process-exporter package version. |
| `process_exporter_web_listen_address` | "0.0.0.0:9256" | Address on which process-exporter will listen |

Dependencies
------------

None.

Example Playbook
----------------

Use it in a playbook as follows:

```yaml
- hosts: all
  become: yes
  roles:
    - process-exporter
```

Configuration notes
-------------------

About usage of process-exporter check:  
https://github.com/ncabatoff/process-exporter/blob/master/README.md

License
-------

BSD

Credits
-------

This role is inspired by https://github.com/cloudalchemy/ansible-mysqld-exporter  
Process-exporter is created by ncabatoff (https://github.com/ncabatoff/process-exporter) and this is only wrap-up in Ansible role.

# Ethereum node installer
Very basic Ansible installation script for Ethereum Parity node on a debian system

## Setup

Ansible version 2.1.0 or greather is required.

Modify the file `hosts` with the correct ip address of the server where you want install parity.

The script needs to connect to the root user via ssh, run:
```
ansible-playbook -i hosts site.yml --ask-pass
```

If you configured the host with your ssh puplic key, you can omit the `--ask-pass` parameter.

The parity daemon could be controlled using the `service` command:
- get status: `service parity status`
- stop: `service parity stop`
- start: `service parity sart`

All parity data is in `/var/lib/parity`, the log file is `/var/lib/parity/parity.log`.


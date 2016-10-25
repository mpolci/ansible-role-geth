# Ethereum node installer
Very basic Ansible installation script for Ethereum node (Parity or Geth) on ubuntu systems.

## Setup

Ansible version 2.1.0 or greather is required.

Modify the file `hosts` adding the hosts you want to install. There are two sections, 
one for hosts with Parity and one for Geth.

The script needs to connect to the root user via ssh and the host should already be in
the local ssh known_hosts file. Run:

```
ansible-playbook -i hosts site.yml --ask-pass
```

If you configured the host with your ssh puplic key, you can omit the `--ask-pass` parameter.

## Daemons 

### Parity
The parity daemon could be controlled using the `service` command:
- get status: `service parity status`
- stop: `service parity stop`
- start: `service parity sart`

All parity data is in `/var/lib/parity`, the log file is `/var/lib/parity/parity.log`.

### Geth
The Geth daemon could be controlled using the `service` command:
- get status: `service geth status`
- stop: `service geth stop`
- start: `service geth sart`

All data is in `/var/lib/geth`. The log is sent to the journal, to show the log messages:

```bash
journalctl --unit geth
```


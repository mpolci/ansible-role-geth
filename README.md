# Ethereum node installer
Very basic Ansible installation script for Ethereum Parity node on a debian system

## Setup

Ansible version 2.1.0 or greather is required.

Modify the file `hosts` with the correct ip address of the server where you want install parity.

The script needs to connect to the root user via ssh, run:
```
ansible-playbook -i hosts site.yml --ask-pass
```

if you configured the host with your ssh puplic key, you can omit the `--ask-pass` parameter.


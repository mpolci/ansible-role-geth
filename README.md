ansible-role-geth
=================

Ansible role for go-ethereum node 

Ansible role
------------

These variables could be configured:

- **geth_user**: user name (default _geth_)
- **geth_group**: group name (default _geth_)
- **geth_bindir**: override geth bin path
- **geth_home**: home for geth service (default _/var/lib/geth_)
- **geth_extra_args**: start parameters

Running system
--------------

The node instance is started by the _geth_ systemd service.

The log is sent to the journal, to show the log messages:

```bash
journalctl --unit geth
```

Uninstall
---------

In order to uninstall geth already installed from this role, you
have to define the tag **uninstall** and the variable **uninstall_geth=true**
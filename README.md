# Deploying Zarb Testnet


## Requirement

- Ubuntu
- python3

Check `ansible.cfg` and `inventory.yml` and update IP address for the remote machine.


## Install dokcer

To install docker on remote machine, run this command:
```
ansible-playbook tasks/install_docker_ubuntu.yml
```

## Generate Keys

Generate two keys without passphrase for sentry and main nodes:

```
zarb key generate
```

Copy the keys under key folder.


## Update nodes:

Check the config files first.
To start or update the node, simply run this command:

```
ansible-playbook tasks/testnet_with_sentry.yml
```

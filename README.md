# Ansible role for OpenSIPS (Compilation from sources)

Ansible role for OpenSIPS (https://www.opensips.org/)

## Tasks
- Choose OpenSIPS version {{ opensips_version }}
- Install dependencies packages
- Create OpenSIPS User and Group
- Clone OpenSIPS repository from GitHub
- Compile from sources
- Install from sources
- Add default, systemd, ... files

## Requirements
- Tested with vagrant box (Debian 8 / 9)
- Ansible 2.7.4

## Start to play
```
service opensips start
```

## Ansible Galaxy
https://galaxy.ansible.com/mickaelh51/ar_opensips_from_sources
```
ansible-galaxy install mickaelh51.ar_opensips_from_sources
```

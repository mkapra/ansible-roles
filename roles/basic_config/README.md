# basic_config

This role is setting up every server with a basic configuration and its
hostname.

## Role Variables

- **hostname**: The hostname of the server -> no default when not defined
- **packages
  ([see defaults](https://github.com/mkapra/ansible-roles/roles/blob/772cf51765c715b0a64d1453d8c4f3d238392ec6/roles/basic_config/vars/main.yml#L3)):**
  This list contains all packages which are getting installed with apt.
- **additional_packages**: Packages to be installed, specified outside this role

## Example Playbook

```yaml
- hosts: servers
  roles:
    - ansible-roles/roles/basic_config
```

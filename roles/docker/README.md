# docker

Install docker and docker-compose (optional).

## Example Playbooks

With docker-compose:

```yaml
- hosts: servers
  vars:
  roles:
    - ansible-roles/roles/docker
```

Without docker-compose:

```yaml
- hosts: servers
  vars:
    install_dockercompose: False
  roles:
    - ansible-roles/roles/docker
```

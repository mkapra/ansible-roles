# update

Full Arch system upgrade via AUR-Helper.

## Role Variables

```yaml
arch_update:
  - AUR_helper: pikaur
    AUR_logfile: ~/pikaur.logs
    AUR_directory: /var/log/pikaur-update/
```

> **Note:** "Write results to logfile (`AUR_logfile:`)" is stored locally (on
> your Ansible machine).

## Example Playbook

```yaml
---
- name: Update all Arch systems
  hosts: allarch

  roles:
    - ansible-roles/roles/arch/update
```

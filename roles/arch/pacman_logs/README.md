# pacman_logs

Check any warnings of pacman. Like `.pacnew` files.

## Example Playbook

```yaml
---
- name: Check pacman log file
  hosts: allarch

  roles:
    - ansible-roles/roles/arch/pacman_logs
```

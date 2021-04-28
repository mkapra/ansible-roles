# mirrorlist

Update Arch mirrorlist.

## Role Variables

```yaml
mirrorlist:
  - country: country=DE
```

## Example Playbook

```yaml
---
- name: Update Arch mirrorlist.
  hosts: arch64

  roles:
    - ansible-roles/roles/arch/mirrorlist
```

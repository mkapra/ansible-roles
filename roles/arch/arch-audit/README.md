# arch-audit

Install arch-audit and run it every day.

> **Note:** Email notification works only with the [msmtp-role](roles/msmtp).

## Role Variables

### Without email notification

```yaml
arch_audit:
  - send_email: false
```

### With email notification

```yaml
arch_audit:
  - send_email: true
    email: email@example.com
```

## Example Playbook

### Without email notification

```yaml
---
- name: Install arch-audit
  hosts: allarch

  roles:
    - ansible-roles/roles/arch/arch-audit
```

### With email notification

```yaml
---
- name: Install arch-audit
  hosts: allarch

  roles:
    - ansible-roles/roles/arch/arch-audit
    - ansible-roles/msmtp/
```

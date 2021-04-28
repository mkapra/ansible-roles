# msmtp

Install msmtp.

## Role Variables

### Minimum

```yaml
msmtp:
  - host: mail.example.com
    from_user: user@example.com
    account_user: user@example.com
    account_user_password: passwd
```

## Example Playbook

```yaml
---
- name: Install msmtp.
  hosts: server

  roles:
    - ansible-roles/roles/msmtp
```

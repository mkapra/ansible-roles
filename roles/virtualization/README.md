# virtualization

Installs KVM with virt-manager.

## Role Variables

**kvm_users**: List all users that want to use KVM in this variable \
**kvm_packages**: Contains all packages to be installed. Do not edit this variable!

## Example Playbook

```yaml
- hosts: servers
  roles:
    - ansible-roles/roles/virtualization
```

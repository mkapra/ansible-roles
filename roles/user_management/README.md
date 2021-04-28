# user-management

This role creates users with its groups (optional) and public keys for SSH
(optional).

## Role Variables

Example for an user:

```yaml
- username: testuser
  usergroup: testuser
  groups:
    - sudo
  hostname_groups:
    - libvirt
  shell: /bin/bash
  pubkeys:
    - ssh-rsa
      AAAAB3NzaC1yc2EAAAADAQABAAABgQCz0fbc97CuOf1uIFyznlWvbkI3F+lIVSc3j6DvDBNyJdCynFsJnidtIslPKQm8/o2lZmzIGQjS5ty2o8hdVN6nag6zy1u7w6ysypAT0XsN7nN8S2qaifPaAPZgcpGwHqv7pMsffOkIOTLXolvYLt7kB936tIP+PmoDUkdS3vm/zKBPi2TQmdHusiwklMmggxT6+vo+RLwudX+Q+4Kt5WARLtX5q5BqzaXAc7joPdip7F7FThaZqE7m9xKBzo9sSkfD7/dsEMnjw/vhXzhtbeYQHIg9XnVM5eK+qAfMui7MzUxh4jqC08RMSQXYgeoZC2zlOX30Y/HFF/WXr+BwO4rNp4m85vNDTiaTwT2YIin1mKXqy8jmeu8gW6wkA3HfB5RxGzK8/E+LNNOenm66+M/YpZis4U+Y4A9TcErwTNO11CWXjp1Y1NpL3WCJWhpf3yp3wTXxTu2+eye9o7S6I+XWqy3IfL3qQPJn97b9G6mh9LQKXjYcxtxXBwdDPcHXkkc=
      testuser@ws
```

The user is only created if a specific variable is created:

```yaml
create_<username>: true
```

Shown in the example above the following line is needed to create the testuser:

```yaml
create_testuser: true
```

Add groups to user on a specific host only:

```yaml
<hostname>_groups:
  - libvirt
```

## Example Playbook

```yaml
- hosts: servers
  roles:
    - ansible-roles/roles/user_management
```

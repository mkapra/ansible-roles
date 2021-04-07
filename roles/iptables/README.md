# iptables

Configures the firewall with the program `iptables`.

## Requirements

- bash
- iptables-persistent

## Role Variables

```yaml
iptables:
  default_input: DROP # Default INPUT Policy
  default_output: ACCEPT # Default OUTPUT Policy
  default_forward: DROP # Default FORWARD Policy
  default_output_iface: eno1 # Default outgoing interface
  allow_established_connections: true # Allow existing connections?
  ip6: true # Allow traffic with IPv4 and IPv6
  flush: true # Flush tables
  restart_docker: true # Restart docker
  restart_wireguard: true # Restart wireguard interfaces for NAT rules
  save_persistent: true # Save rules persistent
  rules:
    - chain: INPUT # Chain where to append the rule
      proto: tcp # Protocol
      dport: 22 # Destination Port
      action: accept # Action
      input_interface: eno1 # Where does the traffic come from?
      output_interface: eno1 # Where should the traffic come out?
```

**Note to `restart_docker` option**: It is important to restart the docker
service if `flush` is set. Docker has to write its own rules into iptables
again.

**Note to `restart_wireguard` option**: It is important to restart the wireguard
interfaces if `flush` is set. Wireguard maybe has to write its own rules into
iptables again (depends on configuration).

## Example Playbook

```yaml
- hosts: servers
  roles:
    - { role: username.rolename, x: 42 }
```

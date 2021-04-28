# wireguard

Configures wireguard interfaces and the configs for its clients. The
configuration files will be located in:

- server: `/etc/wireguard/wg<0-X>.conf`
- clients: `/etc/wireguard/clients/wg<0-X>/<clientname>.conf`

## Role Variables

```yaml
vpns:
  - wg_interface: wg0 # Unique Interface Name
    wg_description: this is a test config for wg0
    wg_v4_address: "192.168.4.1/24" # Internal IP Address Range
    wg_privkey: "" # Private Key of the server. Generate with wg genkey
    wg_listen: "vpn.kapra.de" # IP/Domain to listen on
    wg_nat: true # Should clients to be allowed to reach the internet with NAT?
    wg_nat_interface: ens3 # Outgoing server interface for NAT

clients:
  - client: mac
    ip: "192.168.4.50/24"
    privkey: "" # Private Key of the client. Generate with wg genkey
    allowed_ips: "192.168.4.0/24" # IPs that the client can reach (0.0.0.0/0 for everything into the VPN)
    allowed_client_ip: "192.168.4.2/32" # (IP address of the client)
    vpn: wg0 # Association to an interface/VPN group
```

## Example Playbook

```yaml
- hosts: servers
  roles:
    - ansible-roles/roles/wireguard
```

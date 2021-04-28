# Ansible Roles

Available roles:

- [`basic_config/`](roles/basic_config): Basic configuration for all of my servers
- [`docker/`](roles/docker): Install docker and docker-compose
- [`install_package/`](roles/install_package): Install package/s.
- [`iptables/`](roles/iptables): Configures the firewall with the iptables program
- [`msmtp/`](roles/msmtp): Install msmtp
- [`nginx/`](roles/nginx): Create simple reverse proxy nginx config files
- [`sshd/`](roles/sshd): Configure sshd on a server
- [`user_management/`](roles/user_management): Create users with ssh pubkeys, etc.
- [`virtualization/`](roles/virtualization): Install all packages to virtualize over KVM
- [`wireguard/`](roles/wireguard): Create wireguard configuration for clients and servers

## Specific Arch Linux roles

- [`update`](roles/arch/update): Full Arch system upgrade via AUR-Helper.
- [`arch-audit/`](roles/arch/arch-audit): Install arch-audit and run it every day.
- [`mirrorlist/`](roles/arch/mirrorlist): Update Arch mirrorlist.
- [`mirrorlist-arm/`](roles/arch/mirrorlist-arm): Update Arch ARM mirrorlist.
- [`pacman_logs/`](roles/arch/pacman_logs): Check any warnings of pacman. Like `.pacnew` files.

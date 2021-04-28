# nginx

Configures a nginx webserver as reverse proxy.

## Role Variables

```yaml
# Default server configuration: Every not matching domain will be redirected to this path
nginx_default_server:
  - nginx_server_names:
    nginx_listen_v4:
    nginx_listen_v6:
    nginx_ssl_certificate_path: # Path on the host: Have to be already on the server
    nginx_ssl_certificate_key_path: # Path on the host: Have to be already on the server
    nginx_proxy_pass:

# Simple reverse proxy
nginx_servers:
  - nginx_server_names:
    nginx_listen_v4:
    nginx_listen_v6:
    nginx_ssl_certificate_path: # Path on the host: Have to be already on the server
    nginx_ssl_certificate_key_path: # Path on the host: Have to be already on the server
    nginx_proxy_pass:
    nginx_conf_name:

# Reverse proxy with websocket functionality
nginx_servers_with_websockets:
  - nginx_server_names:
    nginx_listen_v4:
    nginx_listen_v6:
    nginx_ssl_certificate_path: # Path on the host: Have to be already on the server
    nginx_ssl_certificate_key_path: # Path on the host: Have to be already on the server
    nginx_proxy_pass:
    nginx_conf_name:
```

## Example Playbook

```yaml
- hosts: servers
  roles:
    - ansible-roles/roles/nginx
```

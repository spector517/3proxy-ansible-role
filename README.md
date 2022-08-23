"3proxy" Ansible Role
=========

Deploy and configure HTTP and SOCKS proxy server "3proxy"

Requirements
------------

Remotes:
- Based on Debian OS
- Internet connection

Role Variables
--------------

```
# 3Proxy server version
proxy3_version: 0.9.4

# Port of HTTP proxy
proxy3_http_port: 3128

# Port of SOCKS proxy
proxy3_socks_port: 1080

# System user ID and Group ID
proxy3_system_group_id: 200
proxy3_system_user_id: 201

# List of DNS servers
proxy3_dns:
- 1.1.1.1

# true if Uncomplicated Firewall in use
proxy3_use_ufw: false

# Clients of proxy server (accept all connections if empty or undefined)
proxy3_clients:
- name: client0
  password: qwe123
```

Dependencies
------------

The make utility needed on the target hosts.
Also Ansible community module 'make' must be installed.

Example Playbook
----------------

```
- hosts: servers
  roles:
  - role: spector517.3proxy
```

License
-------

MIT

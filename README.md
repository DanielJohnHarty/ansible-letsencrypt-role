# ansible-letsencrypt-role

Ansible role which installs and configures the necessary on a remote server to use the let's encrypt certificate service.

*The current implementation is for ubuntu servers*.

### Usage example

Ansible hosts file:

```
[letsencrypt_server]
server_01
```

Playbook:

```
- hosts: letsencrypt_server
  become: yes
  tasks:
    - name: Set up certificates using let's encrypt service
      import_role: ansible-letsencrypt-role
```
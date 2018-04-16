# Dante SOCKS5 proxy server role for ansible

Create `./library` directory in your ansible project:

```
mkdir ./library
```

And configure `ansible.cfg`:

```
[defaults]
roles_path = ./library
```

Add submodule:

```
git submodule add git@github.com:kressh/ansible-dante.git library/dante
```

Use role:

```yaml
---
- hosts: infra01.yourserver.io
  remote_user: ansible
  become: true
  roles:
    - dante
```

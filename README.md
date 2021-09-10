ansible-role-runc
=================

Ansible role to install runc.

Role Variables
--------------

```yaml
# runc version to install
runc_version: "1.0.2"

# Where to install "runc" binaries.
runc_bin_directory: "/usr/local/bin"

# Owner/group of "runc" binary. If the variables are not set
# the resulting binary will be owned by the current user.
runc_owner: "root"
runc_group: "root"

# Specifies the permissions of the "runc" binary
runc_binary_mode: "0755"

# Processor architecture "runc" should run on.
# Currently only "amd64" is available.
runc_arch: "amd64"

# Name of the binary filename to download
runc_archive: "runc.{{ runc_arch }}"

# The runc download URL (normally no need to change it)
runc_url: "https://github.com/opencontainers/runc/releases/download/v{{ runc_version }}/{{ runc_archive }}"

# SHA256 checksum (see: https://github.com/opencontainers/runc/releases/download/v1.0.2/runc.sha256sum)
runc_checksum: "sha256:44d1ba01a286aaf0b31b4be9c6abc20deab0653d44ecb0d93b4d0d20eac3e0b6"
```

Example Playbook
----------------

```yaml
- hosts: your-host
  roles:
    - githubixx.runc
```

License
-------

GNU GENERAL PUBLIC LICENSE Version 3

Author Information
------------------

[http://www.tauceti.blog](http://www.tauceti.blog)

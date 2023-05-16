# Ansible Role: MongoDB

An Ansible role for installing and configuring MongoDB.

## Requirements

This role requires Ansible 2.10 or later.

## Role Variables

The role uses the following variables, which can be customized in `vars/main.yml` or overridden during playbook execution:

- `mongodb_version`: The version of MongoDB to install (default: `6.0.5`).
- `mongodb_os`: The target operating system for MongoDB (default: `ubuntu1804`).
- `mongodb_os_version`: The specific version of the target operating system (default: `6.0.5`).

## Dependencies

This role has no external dependencies.

## Example Playbook

To use this role, create a playbook as shown below:

```yaml
- name: Install and configure MongoDB
  hosts: servers
  become: true

  roles:
    - role: mongodb
```

You can also override the default variables in the playbook:

```yaml
- name: Install and configure MongoDB
  hosts: servers
  become: true

  roles:
    - role: mongodb
      vars:
        mongodb_version: 4.4.5
        mongodb_os: debian10
        mongodb_os_version: 4.4.5
```

## License

This project is licensed under the [MIT License](LICENSE).

## Author Information

This role was created by Rudolf Olah

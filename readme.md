Ansible Base
============

Base setup of a server.

## Role Variables

- `base_timezone`: Timezone to configure on the host

## Example Playbook

```yaml
- hosts: all
  tasks:
    - ansible.builtin.include_role:
        name: ansible-base
      vars:
        base_timezone: "Europe/Rome"
```

## Build & Publish

To build and publish the role, visit the GitHub Actions page of the repository and trigger the workflow "Release Package" manually.

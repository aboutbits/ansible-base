Ansible Base
============

Base setup of a server.

## Variables

| Variable           | Description                       | Default       |
|--------------------|-----------------------------------|---------------|
| `base_timezone`    | Timezone to configure on the host | `Europe/Rome` |
| `base_auto_update` | Enable automatic package updates  | `true`        |

## Example Playbook

```yaml
- hosts: all
  tasks:
    - ansible.builtin.include_role:
        name: ansible-base
      vars:
        base_timezone: "Europe/Rome"
        base_auto_update: true
```

## Build & Publish

To build and publish the role, visit the GitHub Actions page of the repository and trigger the workflow "Release Package" manually.

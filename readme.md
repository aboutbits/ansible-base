Ansible Base
============

Base setup of a server.

## Role Variables

- `base_timezone`: Timezone to configure on the host
- `base_unattended_update_enabled`: Whether unattended updates should be enabled (default: `true`)
- `base_unattended_reboot_enabled`: Whether unattended upgrades may reboot automatically if needed (default: `true`)
- `base_unattended_reboot_time`: Time when unattended-upgrades should reboot if needed (default: `"05:00"`)
- `base_unattended_reboot_k3s_drain_hook`: Whether to install a k3s drain pre-reboot hook (default: `false`)
- `base_unattended_reboot_k3s_drain_timeout`: Timeout for `k3s kubectl drain` in the optional k3s hook (default: `"120s"`)

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

# Ansible Role: upgrade-packages

This role allow to upgrade the packages and clean unused ones on the system.

* upgrade the packages to the latest version
* clean and autoremove unused packages


---
## Facts Needed

The following facts are needed to get the role to work properly.

* `os_family`
* `distribution`

```yml
- name: Gather Facts
  ansible.builtin.setup:
    gather_subset:
      - '!min'
      - 'os_family'
      - 'distribution'
```


---
## Tags

This roles contains some tags to allow to limit what it does.

* `upgrade` Upgrade the system.


---
## Distributions

This role works for the following distribution families: `Debian` (APT), `RedHat` (DNF).


---
## Usage

Here is an usage example access and setup the role.

```yml
- hosts: all
  gather_facts: no

  pre_tasks:

    # Only gather facts needed for the playbook to save on time.
    - name: Gather Facts
      ansible.builtin.setup:
        gather_subset:
          - '!min'
          - 'os_family'
          - 'distribution'

  tasks:

    # Include the role (if any of the tags are defined)
    - name: Include Role upgrade-packages
      tags: upgrade
      ansible.builtin.include_role:
        name: upgrade-packages
```

You may need to reboot the system afterward.

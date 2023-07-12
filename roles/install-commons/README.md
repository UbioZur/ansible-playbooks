# Ansible Role: install-commons

This role install base packages needed for all systems.

* Cleanup packages that are not needed.
* Install basic packages for the system.


---
## Facts Needed

The following facts are needed to get the role to work properly.

* `os_family`

```yml
- name: Gather Facts
  ansible.builtin.setup:
    gather_subset:
      - '!min'
      - 'os_family'
```


---
## Tags

This roles contains some tags to allow to limit what it does.

* `common-pkgs` Install base packages for the system.



---
## Distributions

This role works for the following distribution families: `Debian` (APT).


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

  tasks:

    # Include the role (if any of the tags are defined)
    - name: Include Role install-commons
      tags: commons-pkgs
      ansible.builtin.include_role:
        name: install-commons
```

You may need to reboot the server to validate the settings.

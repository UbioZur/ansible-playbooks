# Ansible Role: setup-bash

This role setup bash to my liking.

* setup bashrc file
* setup other related files from alias


---
## Tags

This roles contains some tags to allow to limit what it does.

* `bash` Run the whole role.
* `bash-dotfiles` Run only the dotfiles related tasks


---
## Distributions

This role should be distribution independant


---
## Usage

Here is an usage example access and setup the role.

```yml
- hosts: all
  gather_facts: no

  tasks:

    # Include the role (if any of the tags are defined)
    - name: Include Role setup-bash
      tags: bash,bash-dotfiles
      vars:
        setup_bash_user: "USER_TO_SETUP"
      ansible.builtin.include_role:
        name: setup-bash
```

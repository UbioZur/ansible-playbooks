[![Ansible Lint](https://github.com/UbioZur/ansible-playbooks/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/UbioZur/ansible-playbooks/actions/workflows/ansible-lint.yml)

# ⚙️ Ansible Playbooks ⚙️

<img src="https://upload.wikimedia.org/wikipedia/commons/2/24/Ansible_logo.svg" width="75px" align="right" alt="ansible logo" />

My [Ansible](https://github.com/ansible/ansible) playbooks and roles used to deploy, configure and manage systems.

Feel free to use the content of this repository as an **inspiration** or **learning tool** for your own ansible deployement.


---
## 🏁 Quick Start

1. Clone this git repository.

```console
git clone https://github.com/UbioZur/ansible-playbooks.git && cd ansible-playbooks
```

2. Set your [inventories file(s)](inventories/) to manage all of your servers.
3. Copy and edit your [Vault](vault/sample.yml).

```console
cp vaul/sample.yml vault/main.yml
```

4. **[Optional]** Encrypt your vault file.

```console
echo "MY_COMPLICATED_PASSWORD" > vault/.pass
chomod 400 vault/.pass
ansible-vault encrypt --vault-password-file vault/.pass vault/main.yml
```

5. Choose a playbook (see [`Available playbooks`](#-available-playbooks) section).
6. Run `<playbook_name>` with (_or without_) arguments and extra vars:

```console
cd playbooks
ansible-playbook <playbook_name>.yml [args] [extra vars...]
```

7. Enjoy! 😎


## 📚 Available Playbooks

Those playbooks allow to setup or manage the system in a way I like, allowing automation and easier/faster deployment.

- 📖 [`all-gatherfacts`](docs/all-gatherfacts.md) to gather facts and packages of all servers and save them in a local `.json` file.
- 📖 [`omv-setup`](docs/omv-setup.md) to setup Open Media Vault server with the OMV-Extras packages and bash for the CLI interface.


## 🧰 Available Roles

In order to reuse some tasks between playbooks, I am using and sharing the roles with this repositories instead of ansible galaxie.

- 🔧 [`install-commons`](roles/install-commons/README.md) to install commons CLI tools I like to have when I use the system with the command line.
- 🔧 [`setup-bash`](roles/setup-bash/README.md) to setup bash on a user the way I like it (with aliases, prompt etc...).
- 🔧 [`upgrade-packages`](roles/upgrade-packages/README.md) to upgrade the packages on the system.


## 🔭 Project Scope

This project is personal and meant for my personal use and learning purposes. Therefore I will not accept contributions outside of the following:

- **Bug fixing** If there is a bug due to an update in ansible or the system operating system.
- **Best Practices** For learning purposes, I welcome any issues and merge request that will allow me to learn more about best practices with ansible, github, ...
- **Privacy** If I have shared/commit some private information that should stay away from the public eyes.
- **Questions** As I am sharing it for learning purposes, feel free to open a discussion if you have any question related to the playbook or the roles.


## ©️ License

[MIT No Attribution License](LICENSE).

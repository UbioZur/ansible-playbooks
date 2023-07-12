# [←](..) 📖 `omv-setup` playbook

Setup Open Media Vault server with the OMV-Extras packages and bash for the CLI interface.


## Usage

```console
ansible-playbook omv-setup.yml
```


## Tags

- `bash` to install and configure bash (dotfiles)
- `bash-dotfiles` to install bash dotfiles
- `common-pkgs` to install common cli programs to the system.
- `omv-extra` to install omv-extras.
- `sshkey` to add you ssh key to the authorized key file.
- `upgrade` to upgrade the packages on the system.


## Extra Information

Open Media Vault is designed to be configured with the web interface. This playbook is therefore not to configure OMV completly but just to install **OMV-Extras** and make it nicer to connect with SSH.

You should still configure and harden OMV via the web interface!

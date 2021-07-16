# arch-setup

This ansible playbbok is designed to take a fresh install of arch and turn it into a working enviroment with mininimal user intervention

# Dependencies

pacman -S git ansible

ansible-galaxy collection install --ignore-certs community.general

Variables:
--------------

- user: name of computer username
- user_email: email address of you github account
- user_name: name associated with github account
- user_editor: perfered terminal editor of choice
- wireless_network_name: SSID of a wifi network
- wireless_network_password: that networks' password
- ssh_public_key: file name of private ssh key
- password: user password
- password_root: root password
- shell: aboslute pathe to a installed shell like zsh or bash

Tags
--------------------------
adding tags for tasks to be able to skip roles if need be

using the --skip-tags "tag, name"

- user: used for skipping user config
- packages: skipping package installation
- local: skipping local language and time setup
- network: skipping wifi network setup
- services: skipping systemd setup
- git_config: skipping git config
- plugin: skipping installation of plugin managers
- dotfiles: skipping dotfiles

Ansible-Playbook Command
--------------------------

ansible-playbook --ask-vault-pass setup.yml


Steps to  Run after playbook
-----------------------------

get the api key for github cli

add the ssh key generated into your github account

# arch-setup

# Dependencies

pacman -S git ansible

ansible-galaxy collection install community.general

ssh-keygen -C "your_email@example.com"

Variables:
--------------

user: name of computer username
user_email: email address of you github account
user_name: name associated with github account
user_editor: perfered terminal editor of choice
wireless_network_name: SSID of a wifi network
wireless_network_password: that networks' password
ssh_public_key: file name of private ssh key

Ansible-Playbook Command
--------------------------

ansible-playbook --ask-vault-pass setup.yml

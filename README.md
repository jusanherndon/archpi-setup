# arch-setup

# Dependencies
--------------- 

pacman -S git ansible

ansible-galaxy collection install community.general

ssh-keygen -C "your_email@example.com"

Ansible-Playbook Command
--------------------------

ansible-playbook --ask-vault-pass setup.yml

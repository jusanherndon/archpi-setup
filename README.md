# arch-setup

# This ansible playbook assumes you already have git and ansible installed on your system

pacman -S git ansible

ansible-galaxy collection install community.general

ssh-keygen -C "your_email@example.com"
--------------------------

command to run the playbook:

ansible-playbook --ask-vault-pass setup.yml

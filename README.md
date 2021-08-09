# arch-setup

This ansible playbbok is designed to take a fresh install of arch and turn it into a working enviroment with mininimal user intervention

# Dependencies

pacman-key --init

pacman -S git ansible

ansible-galaxy install -r requirements.yml 

(raspberry pi extra dependcies)

pacman-key --populate archlinuxarm

Variables:
--------------

- user: name of computer username
- user_root: name of your root user
- user_email: email address of you github account
- user_name: name associated with github account
- user_editor: perfered terminal editor of choice
- wireless_network_name: SSID of a wifi network
- wireless_network_password: that networks' password
- ssh_public_key: file name of private ssh key
- password: user password
- password_root: root password
- shell: aboslute path to a installed shell like zsh or bash
- user_mergetool: specifying default git merge tool
- user_conflictstyle: specifying default git conflict style
- user_mergetool_prompt: either true or false
- timezone: your local timezone
- groups: list of groups a user could belong to

Ansible-Playbook Command
--------------------------

ansible-playbook --ask-vault-pass setup.yml


Steps to  Run after playbook
-----------------------------

get the api key for github cli

add the ssh key generated into your github account

Command to run to check encrypted Variables
-------------------------------------------

(Be sure to be in the variables folder)

ansible localhost -m ansible.builtin.debug -a var="variable, names" -e "@variable_file.yml" --ask-vault-pass

 
 Command to run to Generate Variable encryption:
 -----------------------------------------------
 
 ansible-vault encrypt_string 'text_needed_to_be_encrypted' --name 'ansible_variable'

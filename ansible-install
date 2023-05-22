#!/usr/bin/env bash

# Install Ansible
sudo apt update -y && sudo apt upgrade -y
sudo apt install -y software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install -y ansible git

# Execute Ansible playbook.
ansible-pull -K -U https://github.com/Kaweees/ansible.git -t setup-machine local.yml
# Or run locally
# ansible-playbook -K local.yml -t setup-machine
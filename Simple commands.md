## List all hosts
ansible all --list-hosts

## Gather information from servers
ansible all -m gather_facts
## Gather information from specific server
ansible all -m gather_facts --limit <IP or hostname>

## Run the playbook (install the apache2 package)
ansible-playbook --ask-become-pass <playbook_name>.yml
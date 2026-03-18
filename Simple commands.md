## List all hosts
ansible all --list-hosts

## Gather information from servers
ansible all -m gather_facts
## Gather information from one server
ansible all -m gather_facts --limit <IP or hostname>
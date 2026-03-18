# ANSIBLE vs ANSIBLE-PLAYBOOK:
- ansible (Ad-Hoc Commands) - used for ad-hoc tasks. Quick, one-off actions not necessarily need to save for later. Perfect for "quick checks" or simple changes across infrastructure.
    Scope: Runs a single task (module) against a set of hosts.
    Best for: Checking connectivity (ping), checking disk space, or restarting a specific service quickly.
    Example: ansible <server_name> -m ping
- ansible-playbook (Automation Scripts) - is the heavy lifter. Executes playbooks, which are YAML files containing a series of "plays" and tasks. Achieve complex configuration management and multi-step deployments.
    Scope: Runs multiple tasks, in a specific order, with logic (variables, loops, handlers).
    Best for: Provisioning a new server, deploying an application, or performing full system upgrades.
    Example: ansible-playbook sys_upgrade.yml
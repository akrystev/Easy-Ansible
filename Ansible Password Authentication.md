# Guide: Using Ansible with Password Authentication

This guide explains how to run Ansible without pre-configured SSH keys by using standard password authentication.

---

## 1. Install Dependencies
Ansible requires the `sshpass` utility to pass passwords to the SSH connection. Install it on your **Control Node**:

* **Ubuntu/Debian:** `sudo apt install sshpass`
* **macOS:** `brew install hudochenkov/sshpass/sshpass`
* **RHEL/CentOS:** `sudo yum install sshpass`

---

## 2. Execution Flags
When running commands, you must explicitly tell Ansible to prompt for passwords using the following flags:

| Flag | Long Form           | Purpose                                                 |
| :--- | :---                | :---                                                    |
| `-k` | `--ask-pass`        | Prompts for the SSH connection password.                |
| `-K` | `--ask-become-pass` | Prompts for the `sudo` (privilege escalation) password. |

### Examples:

**Check if the all hosts are available by using Ping module:**
```bash
ansible all -m ping --ask-pass
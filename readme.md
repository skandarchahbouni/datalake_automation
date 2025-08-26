# 🚀 Ansible Playbooks Setup Guide

## 🔑 Setup SSH Keys

Generate and copy SSH keys to your target hosts:

```bash
ssh-keygen
ssh-copy-id user@<target_host>
```

---

## 📂 Inventory Setup

1. Install **Ansible** if not already installed → [Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
2. Copy the inventory template and update IP addresses:

   ```bash
   cp inventory.template.yml inventory.yml
   ```
3. Edit `inventory.yml` and replace the placeholder IP address with your target host.

---

## ▶️ Running Playbooks

Run the playbooks with your inventory file:

```bash
ansible-playbook -i inventory.yml valkey.yml --ask-become-pass
ansible-playbook -i inventory.yml <playbook>.yml --ask-become-pass
```

---

## ⚠️ Notes

* Ensure **Firewall** is disabled or properly configured with rules.
* Ensure **SELinux** is disabled or configured correctly.


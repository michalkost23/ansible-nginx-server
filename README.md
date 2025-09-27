# Ansible NGINX Server Setup

Tento projekt automatizuje konfiguraci Linuxového serveru s NGINX pomocí Ansible.

## Struktura projektu

- `inventory/` – seznam hostů
- `group_vars/` – proměnné pro hosty
- `playbooks/` – hlavní playbook a role
- `roles/` – jednotlivé Ansible role (common, nginx, ufw, fail2ban, users, webapp)
- `README.md` – tento soubor

## Jak spustit playbook

```bash
ansible-playbook -i inventory/hosts.ini playbooks/site.yml

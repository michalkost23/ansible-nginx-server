# Ansible Web Server Deployment

## Popis
Tento projekt nasazuje jednoduchý web server (NGINX) pomocí Ansible.

- Webové soubory: `/opt/static-sites`
- Web běží pod uživatelem: `webapp`
- Firewall: UFW, povolené porty 22 a 80
- Automatické bezpečnostní aktualizace: aktivní
- Fail2ban: chrání proti brute-force útokům

## Struktura projektu
inventory/
hosts.ini
playbooks/
site.yml
roles/
common/
users/
nginx/
ufw/
fail2ban/
README.md

## Spuštění
```bash
ansible-playbook -i inventory/hosts.ini playbooks/site.yml --become


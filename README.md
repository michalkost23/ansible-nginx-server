This project automates the setup of an NGINX web server on a Linux machine using Ansible. It installs and configures NGINX, sets up a firewall (UFW), creates a dedicated webapp user, enables automatic security updates, and protects the system with Fail2Ban.

The project follows Ansible best practices and includes:
	•	inventory/ – host definitions
	•	group_vars/ – variables for hosts
	•	playbooks/ – main playbook and roles
	•	roles/ – roles for common setup, nginx, ufw, fail2ban, users, and webapp
	•	README.md – documentation and usage guide

Features
	•	Custom NGINX configuration (non-default)
	•	Static web files served from /opt/static-sites (owned by webapp)
	•	Firewall allows only ports 22 and 80
	•	Automatic security updates and Fail2Ban protection
	•	SSH hardened (root login disabled, key-based access only)
	•	Idempotent design – safe to run multiple times
echo -e "\n### How to Run\nRun the Ansible playbook using the following command:\n\`\`\`bash\nansible-playbook -i inventory/hosts.ini playbooks/site.yml\n\`\`\`\n\nTo perform a dry run (check mode without making changes):\n\`\`\`bash\nansible-playbook -i inventory/hosts.ini playbooks/site.yml --check\n\`\`\`" >> README.md

Author: Michal Kost
Assignment: Inizio Technical Task 2025

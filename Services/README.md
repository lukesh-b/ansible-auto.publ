# 🔧 Ansible Services Playbook

This repository contains an Ansible playbook for automating the installation and configuration of essential services on a Linux server fleet. It targets specific groups (e.g., `webservers`, `dbservers`) and uses handlers to start and enable services via `systemd`.

---

## 📋 Features

- Installs **Apache HTTPD** on `webservers`
- Installs **MariaDB** packages on `dbservers`
- Starts and enables services using **Ansible handlers**
- Uses group-based conditional logic
- Uses `systemd` for service management on `dbservers`

---

## 📁 Files

```bash
.
├── services.yml      # Main Ansible playbook
├── hosts             # Static inventory defining host groups
└── README.md         # Project documentation (this file)
```

🚀 How to Use
1. Clone the Repository
```bash
git clone https://github.com/yourusername/ansible-services-playbook.git
cd ansible-services-playbook
```
2. Review or Edit the Inventory
- Update hosts to reflect your infrastructure.

3. Run the Playbook
```bash
ansible-playbook -i hosts services.yml
Make sure Ansible is installed and SSH access is configured to your target hosts.
```

✅ Requirements
Ansible 2.9+ (or later)
RHEL/CentOS-based systems with yum package manager
sudo privileges on target nodes

📝 Notes
```yaml
Handlers are only triggered if the related task causes a change.
The systemd module is used for MariaDB to ensure service compatibility on systemd-based systems.
Modify the playbook if you want to support other distributions (e.g., use apt for Debian/Ubuntu).
```

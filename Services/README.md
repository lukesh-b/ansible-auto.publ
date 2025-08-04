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

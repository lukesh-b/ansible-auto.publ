# disk-prj2/partitioning

An Ansible project to create a 2GB primary partition on `/dev/sdb` and format it with the `ext4` filesystem across multiple Linux hosts.

## 📁 Structure
- `Playbooks` : Different playbooks 
- `hosts`: Inventory file containing group definitions.
- `LICENSE`: MIT license for open-source usage.
- `.gitignore`: Ignore common unwanted files.


## 📋 Prerequisites

- Ansible installed (`ansible --version`)
- SSH access to all inventory hosts
- `/dev/sdb` available and unused on all target machines
- Sudo privileges on the target machines

## 🚀 Usages

###
- `create-primary-partition.yml`:
The Ansible playbook to partition and format the disk.

```bash
ansible-playbook -i hosts create-primary-partition.yml
```

###
`create-logical-partition.yml`
This playbook extends the `/dev/sdb` disk by:

1. Creating an **extended partition** (partition 2) starting just after the end of `/dev/sdb1`
2. Creating a **500 MiB logical partition** (partition 5) within the extended partition

```bash
ansible-playbook -i hosts create-logical-partition.yml
```

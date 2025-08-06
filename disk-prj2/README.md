
# disk-prj2

An Ansible project to create a 2GB primary partition on `/dev/sdb` and format it with the `ext4` filesystem across multiple Linux hosts.

## 📁 Structure

- `create-primary-partition.yml`: The Ansible playbook to partition and format the disk.
- `hosts`: Inventory file containing group definitions.
- `LICENSE`: MIT license for open-source usage.
- `.gitignore`: Ignore common unwanted files.

## 📋 Prerequisites

- Ansible installed (`ansible --version`)
- SSH access to all inventory hosts
- `/dev/sdb` available and unused on all target machines
- Sudo privileges on the target machines

## 🚀 Usage

```bash
ansible-playbook -i hosts create-primary-partition.yml

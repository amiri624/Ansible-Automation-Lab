📄 ansible-lab/README.md

<h1 align="center">🧩 Ansible Automation Lab</h1>

<p align="center">
Automate Nginx & Firewall setup using <b>Ansible</b> — a simple yet powerful DevOps-style lab for system administrators and automation learners.
</p>

---

## 🚀 Overview

This project demonstrates how to automate common Linux server configuration tasks using Ansible.  
It installs and configures:

- 🧱 Basic system packages (vim, curl, net-tools)  
- 🔥 Firewall rules via UFW (SSH & HTTP)  
- 🌐 Nginx web server with a custom template  
- 💾 Deployment of a simple HTML page  

It’s perfect for practicing Ansible roles, inventories, and playbook structures.

---

## 🧭 How to Use

1. Clone this repository:

```bash
   git clone https://github.com/YOURUSERNAME/ansible-lab.git
   cd ansible-lab

2. Edit your inventory file:

[webservers]
localhost ansible_connection=local
# or
# 192.168.56.10 ansible_user=root


3. Run the playbook:

ansible-playbook playbooks/site.yml



---

📂 Project Structure

ansible-lab/
│
├── ansible.cfg              # Global Ansible configuration
├── README.md                # Documentation
│
├── inventory/
│   └── hosts.ini            # Target hosts list
│
├── playbooks/
│   └── site.yml             # Main playbook
│
└── roles/
    ├── common/              # Base setup (system updates, basic tools)
    │   └── tasks/main.yml
    │
    ├── firewall/            # Firewall configuration using UFW
    │   └── tasks/main.yml
    │
    └── nginx/               # Nginx installation and configuration
        ├── tasks/main.yml
        ├── templates/nginx.conf.j2
        └── vars/main.yml


---

⚙️ Requirements

🐧 Linux system (Ubuntu/Debian preferred)

🧰 Ansible installed (sudo apt install ansible -y)

🔑 SSH access to your hosts, or use localhost



---

🧠 What Happens When You Run It

1. Updates and upgrades system packages


2. Installs essential tools


3. Configures UFW to allow SSH and HTTP


4. Installs and configures Nginx


5. Deploys a default HTML page


6. Ensures Nginx service is enabled and running




---

🏁 Example Output

PLAY [Setup Web Servers] ***************************************************************

TASK [Gathering Facts] *****************************************************************
ok: [localhost]

TASK [common : Update apt packages] ****************************************************
changed: [localhost]

TASK [nginx : Ensure nginx is running and enabled] *************************************
ok: [localhost]


---

🧑‍💻 Author: Meisam Amiri
Linux System Administrator / DevOps Engineer


---


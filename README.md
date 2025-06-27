# ☁️ Cloud Server Playbook

A personal knowledge base and toolkit for managing servers and infrastructure across cloud platforms like AWS, Azure, and traditional Linux environments. This repo includes setup guides, command references, automation scripts, and common troubleshooting tips.

---

## 📂 Repository Structure

```
cloud-server-playbook/
├── README.md
├── common/
│   ├── linux-commands.md
│   ├── server-setup.md
│   ├── monitoring-tools.md
│   └── troubleshooting.md
├── aws/
│   ├── ec2.md
│   ├── s3.md
│   ├── cli.md
│   └── iam.md
├── azure/
│   ├── vm.md
│   ├── cli.md
│   └── blob-storage.md
├── linux/
│   ├── networking.md
│   ├── firewall-ufw.md
│   └── ssh.md
├── docker/
│   ├── installation.md
│   ├── common-commands.md
│   └── docker-compose.md
├── nginx/
│   ├── installation.md
│   ├── config-examples.md
│   └── reverse-proxy.md
├── scripts/
│   ├── aws/
│   │   └── create_ec2.sh
│   ├── azure/
│   │   └── setup_vm.sh
│   └── linux/
│       └── setup_server.sh
└── tips-tricks.md
```

---

## 📘 Section Overview

### 🔀 `common/`

Reusable knowledge for any server, across cloud or local environments:

* `linux-commands.md`: Common CLI usage and shell utilities.
* `server-setup.md`: Initial setup tasks like SSH, users, timezone, firewall.
* `monitoring-tools.md`: Tools like `top`, `htop`, `netstat`, etc.
* `troubleshooting.md`: Logs, ports, services, permission errors.

### 🟢 `aws/`

Everything related to AWS:

* Launching EC2, S3 operations, CLI usage, IAM setup.

### 🔵 `azure/`

Instructions for Azure:

* VM setup, storage, Azure CLI basics.

### 🐧 `linux/`

Standalone Linux server tasks:

* Networking basics, UFW firewall, SSH configuration.

### 🐳 `docker/`

Containerization essentials:

* Installing Docker, useful commands, Compose configuration.

### 🌐 `nginx/`

Web server and reverse proxy management:

* Install guide, sample configs, reverse proxy setup.

### 🧰 `scripts/`

Bash automation scripts:

* VM provisioning, EC2 setup, server configuration scripts.

### 💡 `tips-tricks.md`

Handy one-liners, quick fixes, lesser-known but useful tricks.

---

## ✅ Ideal For

* DevOps engineers
* Cloud practitioners
* Self-hosting enthusiasts
* Anyone managing remote servers

---

## 📜 Contribution

Feel free to fork and expand. This is a living document!

---

## 📄 License

MIT License

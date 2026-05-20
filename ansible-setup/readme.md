# 🛠️ Ansible Dev Environment Setup

> Automate your entire developer environment setup with a single command using Ansible.  
> Works on **Linux** and **macOS** natively. Windows users need **WSL**.

---

## 📋 Table of Contents

- [What This Project Does](#-what-this-project-does)
- [Project Structure](#-project-structure)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [How to Run](#-how-to-run)
- [What Gets Installed](#-what-gets-installed)
- [Screenshots](#-screenshots)
- [Customization](#-customization)
- [Troubleshooting](#-troubleshooting)

---

## 🎯 What This Project Does

This Ansible playbook automates setting up a fresh developer machine by:

- Installing essential tools (`git`, `curl`, `vim`, `zsh`, etc.)
- Creating standard project folder structure (`~/projects`, `~/scripts`, etc.)
- Configuring dotfiles (`.bashrc`, `.zshrc`, `.gitconfig`)
- Setting up SSH config
- Installing developer utilities (Node.js, Python pip, etc.)

No more spending hours manually setting up a new machine!

---

## 📁 Project Structure

```
ansible-dev-setup/
├── README.md
├── inventory.ini
├── playbook.yml    # Main playbook
├── roles
│   ├── directories
│   │   └── tasks
│   │       └── main.yml   # Create directory structure
│   ├── dotfiles
│   │   ├── tasks
│   │   │   └── main.yml  # Configure dotfiles
│   │   └── templates
│   │       ├── bashrc.j2     #bashr Config template
│   │       └── gitconfig.j2  # Git config template
│   └── packages
│       └── tasks
│           └── main.yml    # Install packages (git, curl, etc.)
├── screenshots
└── vars
    └── main.yml

```

---

## ✅ Prerequisites

| Requirement | Check Command | Install Guide |
|---|---|---|
| Python 3.x | `python3 --version` | [python.org](https://python.org) |
| Ansible 2.9+ | `ansible --version` | See below |
| Git | `git --version` | [git-scm.com](https://git-scm.com) |

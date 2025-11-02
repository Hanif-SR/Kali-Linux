# 🧩 Kali Linux Installation Overview

This section covers the complete process of setting up **Kali Linux** in a **VirtualBox virtual machine** for safe, isolated cybersecurity practice.  
You’ll find steps for preparing the virtualization environment, installing Kali Linux, and performing initial setup tasks to get the system ready for lab and CTF use.

---

## 📁 Installation Contents

| File | Description |
|------|--------------|
| [`installation-steps.md`](installation-steps.md) | Full step-by-step guide to creating a VirtualBox VM, configuring hardware, installing Kali Linux, and performing post-install tasks. |
| [`troubleshooting.md`](troubleshooting.md) | Common issues during installation and networking setup, and their solutions (e.g., display bugs, adapter errors, missing network connection). |

---

## 🧱 Overview of the Setup Process

### 1️⃣ Prepare Your Environment

Before starting, make sure your system meets the basic requirements:
- Hardware virtualization enabled (VT-x or AMD-V)
- At least **2 CPU cores**, **4 GB RAM** (8 GB recommended), and **40 GB** of disk space
- Installed software:
  - [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
  - [Kali Linux ISO image](https://www.kali.org/get-kali/)

> 💡 Tip: Keep both VirtualBox and the Kali ISO updated to their latest versions for stability and security.

---

### 2️⃣ Create and Configure the Virtual Machine

You’ll create a new VM in VirtualBox and configure its virtual hardware:
- Name and OS type (Linux → Debian 64-bit)
- Allocate sufficient memory and CPU cores
- Create a virtual hard disk (VDI, dynamically allocated)
- Mount the Kali ISO to the virtual optical drive
- Adjust networking for lab usage:
  - **NAT** for internet access  
  - **Host-only / Internal Network** for CTF labs (VulnHub setup)

> 📘 See [`installation-steps.md`](installation-steps.md) for detailed configuration screenshots and network mode explanations.

---

### 3️⃣ Install Kali Linux OS

Boot the VM with the Kali ISO and go through:
- Graphical installation wizard
- Language, region, and keyboard setup
- User creation (non-root account recommended)
- Disk partitioning (guided – use entire disk)
- Bootloader (GRUB) installation
- First login and desktop environment setup

> 🧠 Once installed, take a VirtualBox snapshot so you can revert to a clean state before any major experiments.

---

### 4️⃣ Post-Installation Configuration

After installation, perform initial configuration tasks:
- Update and upgrade system packages:
  ```bash
  sudo apt update && sudo apt full-upgrade -y

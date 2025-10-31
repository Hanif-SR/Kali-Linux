# 🐉 Kali Linux Lab

Welcome to my Kali Linux Lab repository!  
This project documents my journey learning and experimenting with **Kali Linux**, covering installation, configuration, and practical use of cybersecurity tools. It also contains write-ups and notes from CTF-style practice running vulnerable VMs (e.g. from VulnHub) in an isolated lab.

---

## 📦 Contents

- 🧩 [Installation](installation/install_kali_virtualbox.md)
- ⚙️ [Configuration](configuration/network_settings.md)
- 🧠 [Tool Usage](tools/)
- 🧪 [CTF Write-ups](ctf/)
- 🔗 [Resources](resources/useful_links.md)

---

## 🛠️ Tools Covered

- Nmap
- Wireshark
- Metasploit Framework
- Burp Suite
- Hydra
- ffuf

---

## 📚 How I use this repo

| Section | What it contains | How to use it | Example files |
|---|---:|---|---|
| **Installation** | Step-by-step setup for Kali in VirtualBox, post-install actions, Guest Additions, snapshots and networking tips for CTF labs. | Follow before creating your VM. Use snapshots after a clean install and refer to networking tips to safely connect to VulnHub VMs. | `installation/install_kali_virtualbox.md` |
| **Configuration** | Network settings, user & permissions, updating tools, shared folders, and small hardening steps for lab safety. | Apply recommended settings to make the VM usable and safer for lab work; document any changes you make. | `configuration/network_settings.md`, `configuration/updating_tools.md` |
| **Tools** | Individual guides, commands, examples and notes for Nmap, Wireshark, Metasploit, Burp, Hydra, ffuf, etc. | Use as a cheat-sheet while practicing. Copy command examples into your terminal and adapt to each target. | `tools/nmap.md`, `tools/wireshark.md`, `tools/metasploit.md` |
| **CTF / Kali usage on VulnHub** | Walkthroughs and write-ups of CTF-style practice on VulnHub VMs: methodology, commands, screenshots, and lessons learned. | Run vulnerable VMs in an isolated network, follow a write-up template to record methodology and postmortem. Sanitize screenshots/IPs before publishing. | `ctf/template.md`, `ctf/vulnhub-example-1.md` |

---

## ⚠️ Disclaimer

> All activities and tools described here are intended **for educational purposes only**.  
> Only test on systems and networks you own or have explicit permission to test. Respect laws and ethics.

---

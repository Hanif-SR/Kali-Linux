# 🔎 Nmap — Tool Overview

A clean, focused orientation for **Nmap** — what it is, when to use it, and how to think about using it in labs or engagements.  
Practical commands and examples are intentionally **omitted** here so you can add them later in the spots marked **(examples)**.

---

## 📦 Contents

- 🧠 [What is Nmap?](#-what-is-nmap)  
- 🧭 [When to use Nmap](#-when-to-use-nmap)  
- 🛠️ [How to use Nmap (conceptual)](#-how-to-use-nmap-conceptual)  
- 💡 [Tips & Best Practices](#-tips--best-practices)  
- 🔗 [Related files](#-related-files)  
- ⚠️ [Disclaimer](#-disclaimer)

---

## 🧠 What is Nmap?

**Nmap (Network Mapper)** is a powerful and flexible network scanning tool used to discover hosts, enumerate open ports, detect services and versions, and perform basic OS/service fingerprinting.  
It’s a foundational reconnaissance tool that helps map the attack surface before deeper testing.

---

## 🧭 When to use Nmap

Use Nmap early in the reconnaissance phase when you need to:

- Identify which IPs are live on a network.  
- Find open ports and running services on target hosts.  
- Prioritize targets for further analysis (web apps, SSH, SMB, etc.).  
- Create a baseline of network exposure for lab exercises or authorized assessments.  

---

## 🛠️ How to use Nmap (conceptual)

This section gives a concise workflow you can follow in a lab or engagement. Replace the **(examples)** placeholders with specific scan commands when you add practical content.

1. **Host discovery** — determine which addresses respond on a specified range.  
   - *(examples: host discovery commands here)*

2. **Port scanning** — enumerate open TCP/UDP ports on discovered hosts.  
   - *(examples: common scan types here)*

3. **Service & version detection** — probe open ports to identify services and versions.  
   - *(examples: service/version scans here)*

4. **Scripted checks** — leverage Nmap Scripting Engine (NSE) for automated checks (e.g., vuln, auth, discovery scripts).  
   - *(examples: NSE usage here)*

5. **Output & sharing** — save scans in structured formats (normal, XML, grepable) to feed other tools or documentation.  
   - *(examples: output flags/formats here)*

6. **Iterate & refine** — focus subsequent scans on interesting hosts/ports; use timing and targets to reduce noise and speed up testing.  
   - *(examples: targeted scans and timing options here)*

---

## 💡 Tips & Best Practices

- **Start broad, then narrow:** run a light discovery scan first, then deeper scans on interesting hosts.  
- **Use timing templates** (`-T`) to balance speed vs stealth depending on environment.  
- **Leverage NSE scripts** for automated checks but review results manually — scripts can produce false positives.  
- **Export results** (`-oA` or XML) for import into other tools (Metasploit, reporting tools).  
- **Respect targets:** always have explicit permission before scanning networks you do not own.  
- **Avoid noisy scans** in production environments — use low-and-slow settings or run in a lab.

---

## 🔗 Related files

- `tools/` — main tools directory (this file belongs here).  
- `tools/nmap.md` — (this file).  
- `tools/metasploit.md` — recommended follow-up for exploitation workflow.  
- `installation/` — VM setup and lab environment notes (use snapshots before scanning).

---

## ⚠️ Disclaimer

> Nmap is a powerful reconnaissance tool. Use it only on systems and networks you own or have **explicit written permission** to test. Unauthorized scanning may be illegal and unethical.

---

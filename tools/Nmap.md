# 🔎 Nmap — Tool Overview

A clean, focused orientation for **Nmap** — what it is, when to use it, and how to think about using it in labs or engagements.  
Practical commands and examples are intentionally **omitted** here so you can add them later in the spots marked **(examples)**.

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
   - `sudo nmap -sn 192.168.1.0/24`
   - `sudo nmap -sn 192.168.1.1-255`

2. **Port scanning** — enumerate open TCP/UDP ports on discovered hosts.  
   - `sudo nmap -sU -sT 192.168.1.2`

3. **Service & version detection** — probe open ports to identify services and versions.  
   - `sudo nmap -sV 192.168.1.2`

4. **Scripted checks** — leverage Nmap Scripting Engine (NSE) for automated checks (e.g., vuln, auth, discovery scripts).  
   - `sudo nmap -sC 192.168.1.2`

5. **Output & sharing** — save scans in structured formats (normal, XML, grepable) to feed other tools or documentation.  
   - `sudo nmap -sn -n 192.168.1.2 -oG - | awk '/Up$/{print $2}'`

6. **Iterate & refine** — focus subsequent scans on interesting hosts/ports; use timing and targets to reduce noise and speed up testing.  
   - `sudo nmap -sS -T2 -p 1-2000 --scan-delay 200ms 192.168.1.2 -oA quiet_scan`

---

## 💡 Tips & Best Practices

- **Start broad, then narrow:** run a light discovery scan first, then deeper scans on interesting hosts.  
- **Use timing templates** (`-T`) to balance speed vs stealth depending on environment.  
- **Leverage NSE scripts** for automated checks but review results manually — scripts can produce false positives.  
- **Export results** (`-oA` or XML) for import into other tools (Metasploit, reporting tools).  
- **Respect targets:** always have explicit permission before scanning networks you do not own.  
- **Avoid noisy scans** in production environments — use low-and-slow settings or run in a lab.

---

## ⚠️ Disclaimer

> Nmap is a powerful reconnaissance tool. Use it only on systems and networks you own or have **explicit written permission** to test. Unauthorized scanning may be illegal and unethical.

---

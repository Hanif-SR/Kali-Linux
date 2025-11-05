# 🐉 Kali Linux Lab — Tools

A concise orientation to the main Kali tools covered in this repo.
This file explains **what** each tool is, **when** to use it, and **how** to use it at a high level — practical commands are intentionally omitted (not yet). Treat this as a guided map before you dive in.

---

## 📦 Contents

* 🧠 [Tool Overviews](#-tool-overviews)
* 🧭 [How to Use This Tool (conceptual)](#-how-to-use-this-tool-conceptual)
* 🔍 [When to Use Each Tool](#-when-to-use-each-tool)

---

## 🛠️ Tools Covered

* Nmap
* Whatweb
* Burp Suite
* Hydra
* ffuf

---

## 🧠 Tool Overviews

Below are short orientations for each tool — what it does and the role it plays in typical security work / lab exercises. Each entry also includes a **How to use (conceptual)** subsection.

---

### Nmap — network discovery & reconnaissance

**What it is:** A powerful network scanner used to discover hosts, open ports, running services, and basic OS/service fingerprints.
**Role:** First-step reconnaissance — map the attack surface, identify live hosts and exposed services.

**How to use (conceptual)**

1. **Host discovery:** Identify live IPs in the target range.
2. **Port scanning:** Enumerate open ports on discovered hosts.
3. **Service detection:** Probe ports to determine services and versions.
4. **Save & prioritize:** Export results and focus on interesting hosts/services.
5. **Iterate:** Run targeted scripts and narrower scans based on findings.

---

### Whatweb — web technology fingerprinting

**What it is:** A web scanner that identifies technologies used by a website (CMS, server, frameworks, analytics, plugins, headers, etc.).
**Role:** Rapid technology reconnaissance for web targets — helps prioritize follow-up testing by revealing frameworks, CMS versions, and exposed components.

**How to use (conceptual)**

1. **Point at web endpoints** discovered during reconnaissance.
2. **Fingerprint technologies** (server types, CMS, frameworks, libraries).
3. **Correlate results** with known CVEs or version-specific checks.
4. **Feed insights** to Burp and ffuf to select targeted payloads/wordlists.
5. **Iterate** as you uncover additional subdomains or virtual hosts.

---

### Burp Suite — web application proxy & testing platform

**What it is:** An intercepting HTTP(S) proxy with tools (Proxy, Repeater, Intruder, Scanner) for inspecting and manipulating web traffic.
**Role:** Manual and semi-automated web application testing — observe requests/responses, tamper with parameters, and validate vulnerabilities.

**How to use (conceptual)**

1. **Configure browser proxy** and import Burp CA for HTTPS.
2. **Intercept traffic** to inspect requests/responses.
3. **Analyze flows** and identify interesting parameters.
4. **Tamper** with requests in Repeater; automate in Intruder where needed.
5. **Scope** your target to avoid noise/out-of-scope testing.
6. **Verify** findings manually and document them.

---

### Hydra — parallelized login cracker

**What it is:** A fast credential brute-forcing tool for many network protocols (SSH, FTP, HTTP forms, RDP, etc.).
**Role:** Credential testing — validate weak passwords and authentication policies in a controlled environment.

**How to use (conceptual)**

1. **Identify auth endpoints** during recon (SSH, web forms, etc.).
2. **Choose attack mode** (single user, user list, password list).
3. **Prepare wordlists** tailored to the target.
4. **Limit parallelism** to avoid lockouts or DOS (`-t`).
5. **Run safely in a lab** and monitor service health.
6. **Handle results responsibly** (report and remediate).

---

### ffuf — fast web fuzzer / discovery tool

**What it is:** A lightweight, high-performance fuzzer for discovering directories, files, parameters, and virtual hosts on web servers.
**Role:** Content discovery and fuzzing — find hidden endpoints, backup files, or parameterized inputs not linked in the application.

**How to use (conceptual)**

1. **Pick fuzz points** (path, parameter, host header).
2. **Select wordlists** relevant to the target.
3. **Run focused fuzzing** and start with common lists.
4. **Filter results** by status code/size to reduce false positives.
5. **Verify findings** manually (Burp/browser).
6. **Iterate** with customized lists based on patterns discovered.

---

## 🧭 How to Use These Tool

This section summarizes the **practical mental model** for using each tool in a lab or engagement. Use it as a quick decision map.

* **Nmap:** Start here. Use it to find live hosts, open ports, and services. Export scans to feed other tools.
* **Burp Suite:** Use for web app traffic inspection and manual testing. Intercept, tamper, and validate web vulnerabilities.
* **ffuf:** Use after initial mapping to discover hidden endpoints and content. Great for directories, vhosts, and fuzzing parameters.
* **Hydra:** Use for controlled credential testing only when you have authorization; start with targeted lists and conservative parallelism.
* **Whatweb:** Use to quickly fingerprint web technologies and versions — informs targeted exploits, wordlists, and Burp scripts.

---

## 🔍 When to Use Each Tool

| Phase in a lab / engagement        |            Tool(s) to reach for | Why / what you'll learn                                                                |
| ---------------------------------- | ------------------------------: | -------------------------------------------------------------------------------------- |
| **Initial reconnaissance**         |                          `Nmap` | Discover live hosts, open ports, and services.                                         |
| **Web application recon**          | `Burp Suite`, `ffuf`, `Whatweb` | Intercept/inspect traffic, find hidden endpoints, and fingerprint tech stacks.         |
| **Credential assessment**          |                         `Hydra` | Test password strength and authentication policies.                                    |
| **Exploit validation / targeting** | `Whatweb`, `Nmap`, `Burp Suite` | Use fingerprints and service versions to prioritize exploits or further investigation. |
| **Deeper discovery & fuzzing**     |            `ffuf`, `Burp Suite` | Find undocumented surfaces, parameters, and content leakage.                           |

---

## ⚠️ Disclaimer

> All activities and tools described here are intended **for educational purposes only**.
> Only test systems and networks you **own** or have **explicit permission** to test. Respect laws, privacy, and ethics.

---


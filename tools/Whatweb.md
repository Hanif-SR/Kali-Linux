# 🔎 WhatWeb — Tool Overview

A clean, focused orientation for **WhatWeb** — what it is, when to use it, and how to think about using it in labs or engagements.
Practical commands and examples are included below so you can drop them into your lab notes. Replace example targets with your own lab IPs / domains.

---

## 🧠 What is WhatWeb?

**WhatWeb** ("What is that Website?") is a fast web technology fingerprinting tool that identifies web servers, CMSs, frameworks, JavaScript libraries, analytics, headers, plugins, and (when available) version numbers and other metadata.
It uses a large plugin collection to detect hundreds to thousands of web technologies and can be run at different aggression levels for speed vs. depth.

---

## 🧭 When to use WhatWeb

Reach for WhatWeb when you want to:

* Quickly fingerprint the technology stack of a web endpoint (CMS, server, frameworks).
* Prioritize follow-up testing with Burp/ffuf based on detected tech and versions.
* Build a map of technology coverage across multiple hosts or subdomains.
* Triage targets by spotting out-of-date or fingerprintable components that often have public CVEs.

---

## 🛠️ How to use WhatWeb (practical)

Follow this concise workflow in a lab or assessment. Practical command examples are provided directly under each step.

1. **Point at web endpoints** — run a single-site fingerprint to get a quick tech summary.

   * `whatweb -v https://example.com`
   * `whatweb http://192.168.1.10:8080`

2. **Scan many hosts** — feed a list of targets to fingerprint many sites in one pass.

   * `whatweb --input-file targets.txt`
   * `whatweb -i targets.txt -a 1`  # `-a` sets aggression level

3. **Adjust aggression** — increase aggression (`-a`) to run deeper checks (may be slower/noisier).

   * `whatweb -a 3 example.com`  # higher aggression for more details

4. **Verbose output & error handling** — enable verbose output and suppress noisy errors for large scans.

   * `whatweb -v example.com --no-errors`
   * `whatweb --no-errors 192.168.0.0/24`

5. **Export structured logs** — save results in machine-readable formats (XML, JSON, brief) for later parsing or ingestion.

   * `whatweb -v example.com --log-xml=site-scan.xml`
   * `whatweb -i targets.txt --log-json=site-list.json`
   * `whatweb example.com --log-brief=brief.txt`

6. **Use plugin & list tools** — inspect available plugins and limit or extend plugins if needed.

   * `whatweb --list-plugins`
   * `whatweb --max-plugins 100 example.com`

7. **Correlate results** — combine fingerprints with CVE databases, Burp findings, or ffuf discoveries to prioritize follow-ups.

   * (Example workflow) `whatweb` → identify “Drupal 7” → search CVEs → prioritize exploits or patch checks.

---

## 💡 Use example

* Fingerprint a single site (verbose):

```bash
whatweb -v https://example.com
```

* Fingerprint using higher aggression (deeper checks):

```bash
whatweb -a 3 https://example.com
```

* Fingerprint a list of targets from `targets.txt` (one URL per line):

```bash
whatweb --input-file targets.txt --no-errors --log-brief=results.brief
```

* Save JSON and XML output for automation:

```bash
whatweb -i targets.txt --log-json=results.json --log-xml=results.xml
```

* Run moderate scan, limit plugins (speed control):

```bash
whatweb -a 2 --max-plugins 200 example.com
```

* Get a list of available plugins (helps craft targeted scans):

```bash
whatweb --list-plugins
```

---

## ⚙️ Tips & Best Practices

* **Start conservative:** use low aggression (`-a 0` or `-a 1`) on production-like targets; increase only in lab environments.
* **Hit lists, not blind scans:** prefer targeted lists (`--input-file`) rather than sweeping large external ranges without permission.
* **Combine tools:** use WhatWeb to inform Burp and ffuf workflows (e.g., use detected CMS to pick wordlists).
* **Log structurally:** always save JSON/XML when scanning many hosts — it makes automation and reporting trivial.
* **Respect rate & noise:** WhatWeb is lighter than active exploit scans, but higher aggression levels probe deeper — be mindful.
* **Verify findings:** WhatWeb fingerprints are a starting point — manually verify interesting results in Burp/browser.

---

## ⚠️ Disclaimer

> WhatWeb is a reconnaissance tool intended **for authorized testing and learning**. Only run it against systems you own or have **explicit written permission** to test. Unauthorized scanning can be illegal and unethical.

---

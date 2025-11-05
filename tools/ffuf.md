# 🔎 ffuf — Tool Overview

A concise, professional overview of **ffuf**: its purpose, typical use cases, and a compact operational workflow suitable for laboratory exercises and authorized assessments. Emphasis is placed on focused operation, reproducibility, and minimizing collateral impact.

---

## 🧠 What is ffuf?

**ffuf (Fuzz Faster U Fool)** is a fast, flexible web fuzzer designed for content discovery: directory/file brute-forcing, parameter discovery, virtual host enumeration, and general HTTP surface probing. It is optimized for high throughput, easy filtering of noisy responses, and straightforward output formats for automation.

---

## 🧭 When to use ffuf

* Discover hidden paths, backup files, and administrative endpoints on web servers.
* Enumerate parameters or file names that are not linked in the application.
* Probe virtual hosts or subdomain permutations via Host header/fuzzing.
* Rapidly triage multiple hosts with structured output for later analysis.

---

## 🛠️ How to use ffuf 

1. **Pick the fuzz point** — decide whether to fuzz path, parameter, or hostname (Host header).
2. **Select wordlists** — start with small, curated lists (common directories) then expand to medium/large lists as needed.
3. **Set match/filter rules** — use status codes, response size, word counts, or regex to reduce false positives.
4. **Control concurrency** — tune threads to balance speed vs. target load; begin conservatively in production-like environments.
5. **Persist structured output** — export JSON (or other supported formats) for ingestion into reporting pipelines.
6. **Verify findings** — manually confirm interesting results (browser / Burp Suite) before documenting.

---

## Use example

> Replace example domains, paths, and wordlists with items from your authorized lab.

* Basic directory fuzz (common wordlist):

```bash
ffuf -u https://example.com/FUZZ -w /usr/share/wordlists/dirb/common.txt -t 40 -mc 200 -o ffuf_basic.json -of json
```

* Fuzz with extensions and filter 404 responses:

```bash
ffuf -u https://example.com/FUZZ -w wordlists/big.txt -e .php,.bak,.old -mc 200 -fc 404 -t 50 -o ffuf_ext.json -of json
```

* Virtual-host (vhost) discovery via Host header:

```bash
ffuf -u https://example.com/ -H "Host: FUZZ.example.com" -w wordlists/vhosts.txt -t 60 -mc 200 -o ffuf_vhost.json -of json
```

* Parameter fuzzing (query parameter):

```bash
ffuf -u 'https://example.com/search?q=FUZZ' -w wordlists/params.txt -t 30 -mc 200 -o ffuf_param.json -of json
```

* Recursive fuzzing (deeper discovery):

```bash
ffuf -u https://example.com/FUZZ -w wordlists/common.txt -recursion -recursion-depth 2 -t 30 -mc 200 -o ffuf_recursive.json -of json
```

* Filter by response size to reduce noise:

```bash
ffuf -u https://example.com/FUZZ -w wordlists/common.txt -fs 1234 -t 40 -o ffuf_sizefilter.json -of json
```

---

## ⚠️ Disclaimer

> ffuf is a powerful reconnaissance tool. Use it only on systems and networks for which you have **explicit written authorization**. Unauthorized fuzzing or aggressive probing may be illegal, disruptive, and unethical.

---

# HSociety Recon Toolkit ⚡

A lightweight, automated reconnaissance script built to streamline **legitimate domain analysis**, OSINT collection, and service fingerprinting. Outputs are neatly organized into a timestamped folder for easy review.

---

## Features

### • WHOIS Collection  
Gathers registrar metadata, name servers, contact details, and other publicly available domain info.

### • DNS Enumeration  
Captures:
- A / AAAA  
- NS  
- MX  
- TXT  

All saved in a clean `dns.txt` file.

### • Subdomain Brute Force  
Parallelized brute‑forcing using a common wordlist.  
Automatically resolves valid hosts and maps them to IPs.

### • Nmap Scanning  
Runs:
- Top 1000 ports  
- Service detection  
- Fast timing mode (`-T4`)  

Results saved to `nmap.txt`.

### • TLS Certificate Info  
Extracts:
- Issuer  
- Subject  
- NotBefore / NotAfter  
- SAN entries  

Pulled directly with OpenSSL.

### • HTTP/HTTPS Metadata  
Fetches:
- Response headers  
- `robots.txt` where available  
- Saves files separately for both schemes

---

## Requirements

This script depends on:

- `whois`  
- `dig`  
- `curl`  
- `openssl`  
- `nmap`  

Optional:
- `/usr/share/wordlists/dirb/common.txt` (for subdomain brute‑forcing)

Make sure they’re installed via your package manager.

---

## Usage

```bash
./hs_recon.sh <domain>

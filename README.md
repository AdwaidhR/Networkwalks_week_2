# NetworkWalks Cybersecurity Internship — Week 2

**Name:** Adwaidh R  
**Batch:** B084C  
**Week:** 2  
**Modules:** W2-PM1 (Footprinting with Kali Linux tools), W2-PM5 (Zenmap-based Network Scanning), and W2-PM-FINAL (Detailed Report).

## Repository structure

- `Report/Adwaidh_R_NetworkWalks_Week2_Report.docx` — detailed report covering the selected modules.
- `Screenshots/PM1-Footprinting/` — evidence from the six footprinting tools.
- `Screenshots/PM5-Zenmap/` — host discovery, TCP/UDP scans, service detection, and topology evidence.

## W2-PM1 — Footprinting

The assigned domain `networkwalks.com` was examined using the following tools:

| Tool | Purpose / observed result |
|---|---|
| WHOIS | Domain registration and nameserver details |
| WhatWeb | Web technology fingerprinting; HTTP 200 and WordPress-related components observed |
| Nslookup | DNS lookup; A record resolved to `192.232.216.135` |
| cURL | HTTP response headers; HTTP/2 200 observed |
| wafw00f | ModSecurity WAF detected (SpiderLabs) |
| DNSRecon | DNS record enumeration; eight records reported |

## W2-PM5 — Zenmap / Nmap

Scanning was performed against the learner's own VirtualBox NAT Network (`10.0.0.0/24`).

- Host discovery identified `10.0.0.1`, `10.0.0.2`, and `10.0.0.3` as up.
- `10.0.0.2` was the Kali VM; `10.0.0.1` was the NAT Network gateway.
- Service detection reported TCP 80 and 3306 on `10.0.0.1`, and TCP 53 on `10.0.0.3`; the DNS service was fingerprinted as dnsmasq 2.45.
- UDP results reported UDP 69 on `10.0.0.1` and UDP 53 on `10.0.0.3`.
- The exact identity of `10.0.0.3` was not independently confirmed.

## Scope and responsible testing

Footprinting was limited to the assigned training domain using information-gathering techniques. Network scanning was limited to the learner's own local VirtualBox NAT Network. The results describe only what the tools reported during the tests and do not identify the unknown host beyond the observed scan evidence.

## Full report

See [`Report/Adwaidh_R_NetworkWalks_Week2_Report.docx`](Report/Adwaidh_R_NetworkWalks_Week2_Report.docx).

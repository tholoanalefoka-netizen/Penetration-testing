PENETRATION TESTING REPORT

Footprinting & Network Scanning Phases
W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS

| Phase | Module | What it does |
|---|---|---|
| **Reconnaissance / Footprinting** | `W2-PM1` | Profile `networkwalks.com` using 6 built-in Kali Linux tools |
| **Scanning / Network Discovery** | `W2-PM5` | Discover live hosts on my own local network with Zenmap |

 Passive reconnaissance (footprinting) — reading public data without touching the target
 
 Domain & DNS intelligence — WHOIS, name servers, DNS records, mail servers
 
 WAF (Web Application Firewall) detection
 
 Host discovery & network mapping — ping sweeps, live-host enumeration
 
 MAC addressing & vendor identification (and MAC randomization as a privacy defense)
 
 Reporting & risk analysis — turning findings into documented, actionable risk

 1.FOOTPRINTING

 Footprinting, also known as reconnaissance, is the first phase of a cybersecurity assessment or cyberattack. It involves gathering as much information as possible about a target system, network, or organization to map out its digital footprint and identify potential vulnerabilities before launching an actual attack or deeper scan.

The goal is to build a detailed profile of the target's security posture and attack surface. Footprinting is generally divided into two categories:

* **Passive Footprinting:** Gathering information without directly interacting with the target's servers or networks. As noted in your document, this involves "reading public data without touching the target." Methods include searching public records (OSINT), WHOIS database lookups, analyzing social media for employee details, and reviewing job postings to see what technologies a company uses.
* **Active Footprinting:** Directly interacting with the target to gather information. This leaves a trace and can potentially be detected by the target's security systems. Methods include ping sweeps (to see which hosts are alive), port scanning, and DNS zone transfers.

**Common data collected during footprinting includes:**

* Domain names and internal/external IP addresses
* Network topology and routing information
* Operating systems and software versions in use
* Employee names, email addresses, and phone numbers
* Security mechanisms in place (like Web Application Firewalls or intrusion detection systems)

## Module 1 — Footprinting with 6 Kali Tools (W2-PM1)

Six built-in Kali tools, each revealing a different layer of the target. Every finding cross-confirmed the others from independent sources.

| # | Tool | Question it answers | Layer |
|---|------|--------------------|-------|
| 1 | `whois` | Who owns the domain? | Ownership |
| 2 | `whatweb` | What software does it run? | Tech stack |
| 3 | `nslookup` | What is its real IP? | Location |
| 4 | `curl -I` | What does the server reveal? | Server banner |
| 5 | `wafw00f` | Is a firewall watching? | Defenses |
| 6 | `dnsrecon` | What is the full DNS map? | Infrastructure |

 ## Module 2 — Network Scanning with Zenmap (W2-PM5)
 
 For the second activity, I used Zenmap to perform network discovery on my local network. The practical required me to identify my local IP address and subnet, discover live hosts, identify their IP and MAC addresses, and generate a network topology.

 I used the network configurations I made in week 1 for my linux machine to search for the devices in my network.
 After completing the scan, I opened the Topology section in Zenmap, enabled the legend and saved the network topology in PDF format as required by the practical task.

 ## Conclusion

During Week 2 of my Cybersecurity & Ethical Hacking internship, I completed practical activities covering footprinting, reconnaissance and network scanning.

In the footprinting activity, I used six Kali Linux tools to collect information about the target domain. I learned how WHOIS can provide domain information, WhatWeb can identify web technologies, Nslookup can resolve domain names, Curl can inspect HTTP headers, Wafw00f can identify a WAF, and DNSRecon can provide additional DNS information.

In the network scanning activity, I used Zenmap to identify my local network configuration and discover active hosts. I also collected IP and MAC address information and created a network topology.

The exercises showed me that information gathering is an important part of cybersecurity. Even before attempting to exploit a system, a security professional can learn a significant amount about an environment by carefully analyzing publicly available information and network responses.

I also learned that technical findings should be documented clearly. A good cybersecurity report should explain what was performed, what was discovered, what the observation means, what risk it may create, and what can be done to reduce that risk.

Finally, I learned that reconnaissance and scanning must always be performed within an authorized scope. These activities were completed as part of the assigned educational cybersecurity lab.

 ## Author

**Tholoana Lefoka**
Cybersecurity &amp; Ethical Hacking Intern — NetworkWalks, Batch 84

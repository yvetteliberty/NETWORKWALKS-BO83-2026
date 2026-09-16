# 🧰 FOOTPRINTING AND NETWORK SCANNING PHASES
## Footprinting is the information-gathering phase of cybersecurity reconnaissance. It involves collecting details about a target before attempting further security testing.
## Network scanning is the process of examining a network to identify active hosts, open ports, running services, and potential weaknesses.

# 📌 Project Review
 This project covers foot printing of the networkwalks.com domain using multiple Kali Linux tools (W2-PM1) ,theharvester (W2-PM4) on microsoft.com and scanning my own local network with Zenmap (W2-PM5). The two modules which includes theharvester scanning and multiple kali linux tools(whois, dnsrecon,whatweb,curl,wafw00f) covers the footprinting phase and the zenmap  covers the scanning phase, so together they show how an attacker moves from gathering public information to mapping live hosts on a network. It is the Week 2 part of my ongoing internship program at Networkwalks.
All commands were run in Kali Linux (footprinting) and on a Windows PC with Zenmap installed (scanning). Every step below includes the exact command used, the result I observed, a screenshot as evidence, and a short note on why the finding matters from an attacker's point of view a documented report based on all finds and recommendations.

# 🎯Objectives
The Purpose is to understand the use of the following tools for footprint reconnaissance
- WHOIS
- WHATWEB
- CURL
- NSLOOKUP
- WAFWOOF
- DNSRECON on target IPs and domain name /URLS.
## Network scanning
  - Download and install zenmap
  - Scan my personal Pc
  - Identify  it local  lan IP address ,subnet
  - Identify  live hosts and MAC addresses.

# 🛡️Purpose of this Project
The purpose of this project is to perform authorized reconnaissance and network scanning to gather information about a target system and identify its exposed infrastructure, services, and technologies. The project uses reconnaissance commands and tools such as WHOIS, WhatWeb, DNSRecon, NSLookup, theHarvester, cURL, and Wafw00f to collect domain information, DNS records, web technologies, email or subdomain information, HTTP details, and web application firewall (WAF) information. This helps develop practical skills in cybersecurity reconnaissance, information gathering, and network security assessment

# 🧰 Tools Use for this Project

| Tool | Purpose |
|---|---|
| Kali Linux & Windows | Operating systems used for reconnaissance activities |
| WHOIS | Find domain registration details such as owner, dates, registrar, and name servers |
| WhatWeb | Fingerprint web technologies such as server, CMS, plugins, and IP information |
| NSLookup | Resolve domain names to IP addresses using DNS |
| cURL (`curl -I`) | Retrieve and analyze HTTP response headers from a website |
| Wafw00f | Detect whether a Web Application Firewall (WAF) protects a website |
| DNSRecon | Enumerate DNS records such as NS, MX, SPF, TXT, and SRV |
| Zenmap (Nmap GUI) | Scan an authorized local subnet to identify live hosts, IP addresses, and MAC addresses |
| Windows CMD | Identify local IP address, MAC address, and network configuration |
| theHarvester | Gather publicly available information such as emails, subdomains, hostnames, IP addresses, and other reconnaissance data |

# 🎯 Activity Performed.
## Footprinting & Reconnaissance
I performed reconnaissance against the networkwalks.com domain using six Kali Linux tools: whois, whatweb, Nslookup, Curl, Wafw00f and DNSRecon. Each tool was used to collect a different type of information about the target.
First, I used WHOIS to obtain publicly available domain registration information and identify the domain’s name servers. The results provided information about the domain registration and hosting infrastructure.
Then  I used WhatWeb to identify technologies used by the website. The results identified WordPress 7.1 and WP Download Manager [3.3.58], HTTPSERVER(Apache), Bootstrap[ 7.1] ,JQUERY[3.7.1], IP address :192.232.216.135  and along with other information exposed by the website.
Using Nslookup, I resolved the domain name to its IP address. The provided result identified 192.232.216.135.
I used Curl with the -I option to inspect the HTTP response headers. This provided additional information about the web application and exposed the WordPress REST API endpoint /wp-json/ and the server.
Next, I used Wafw00f to determine whether a Web Application Firewall was protecting the website. The result identified ModSecurity (SpiderLabs).
Finally, I used DNSRecon to enumerate DNS records. The results provided information relating to name servers, mail servers, SPF/TXT records, service records and DNS software information.


## TheHarvester Scanning.
I performed another footprinting scan on Microsoft .com. This tool revealed the email addresses, IPaddresses, sub-domains found in Microsoft .com. This information’s are revealed through different source like baidu, ebay and other related search engineers.


## Network Scanning with Zenmap
For the second activity, I used Zenmap to perform network discovery on my local network. The practical required me to identify my local IP address and subnet, discover live hosts, identify their IP and MAC addresses, and generate a network topology.
I first used the Windows ipconfig command to identify my local IP address and LAN subnet. I then entered the subnet into Zenmap and selected Ping Scan to identify active hosts.
The results provided in the practical identified two live hosts:
- 172.17.155.56
- 172.17.155.63
- MAC addresses were Unavailable.

After completing the scan, I opened the Topology section in Zenmap, enabled the legend and saved the network topology in PDF format as required by the practical task.




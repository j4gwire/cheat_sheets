# Passive Recon Cheat Sheet

## Search Engines

| Search Engine | Description                                                         |
|---------------|---------------------------------------------------------------------|
| Google, Bing, DuckDuckGo, Yahoo, Blekko, Yandex... | Popular search engines for gathering information. |
| **Search Terms** | `"company name" + password filetype:xls` (example search term) |
| **Google Hacking Database** | [www.exploit-db.com/google-hacking-database](http://www.exploit-db.com/google-hacking-database) |

## Information of Interest

| Area of Interest      | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
| **Geographical Locations** | Office locations and geographic data of the target.              |
| **Company Overview** | Subsidiary companies, mergers, acquisitions, etc.                    |
| **Employee Names & PII** | Contact information, emails, phone numbers, and other PII.        |
| **Business Partners & Vendors** | Relationships with third-party vendors or partners.        |
| **Technology in Use** | Software, hardware, and technologies used by the target.            |

## Online Sources

| Source              | Description                                                         |
|---------------------|---------------------------------------------------------------------|
| LinkedIn, Jigsaw, Facebook, Twitter, Google+, Seek, Blogs, Usenet | Common social media and online platforms to gather information. |
| **WayBack Machine**  | [archive.org](http://archive.org) - View historical versions of websites. |
| **Search Engine Directory** | [searchenginecolossus.com](http://searchenginecolossus.com) |
| **Zuula**            | [www.zuula.com](http://www.zuula.com) - Meta search engine.          |
| **DNSstuff**         | [www.dnsstuff.com](http://www.dnsstuff.com) - DNS lookup tools.      |
| **ServerSniff**      | [www.serversniff.net](http://www.serversniff.net) - Information on servers. |
| **Netcraft**         | [www.netcraft.com](http://www.netcraft.com) - Web server information. |
| **My IP Neighbors**  | [www.myIPneighbors.com](http://www.myIPneighbors.com) - Find IP neighbors. |
| **Shodan**           | [www.shodanHQ.com](http://www.shodanHQ.com) - Internet of Things and device search engine. |

## Password Dumps

| Source              | Description                                                         |
|---------------------|---------------------------------------------------------------------|
| **Password Dumps**   | `site:pastebin.com "targetURL"` - Search for dumps related to the target. |

## DNS Recon

DNS is a distributed database that resolves domains to IP addresses.

| Command            | Description                                                         |
|--------------------|---------------------------------------------------------------------|
| `nslookup targeturl.com` | Standard DNS lookup.                                                |
| `dig targeturl.com` | Detailed DNS query.                                                 |

### Zone Transfer
A zone transfer may provide hostnames & IP addresses of Internet-accessible systems.

> **Note**: A zone transfer request may trigger IDS/IPS alarms.

### Vulnerable Services

Misconfigured, unpatched servers (e.g., `dbase.test.target.com`).

### DKIM and SPF Records
Used to control spam emails and impact phishing/social engineering attacks.

## Whois

| Command            | Description                                                         |
|--------------------|---------------------------------------------------------------------|
| `whois targeturl.com` | Look up domain registration details.                                 |

## Social Engineering

| Attack Type        | Description                                                         |
|--------------------|---------------------------------------------------------------------|
| **Identify locations for physical attacks** | Identify office or building locations.                       |
| **Phone numbers**  | War dialing attacks to discover numbers.                            |
| **Domain Seizure** | Attempt to seize domains and create look-alike websites.            |

## IPv6

| Description        | Details                                                            |
|--------------------|--------------------------------------------------------------------|
| **Misconfigurations** | May leak data and bypass old firewalls/IDS/IPS.                    |
| **dnsdict6**       | `dnsdict6 -4 targeturl.com` - Enumerates subdomains for IPv4/IPv6. |
| **dnsrevenum6**    | `dnsrevenum6 dnsip ipv6address` - Reverse DNS for IPv6 addresses.  |

## IPv4

| Command            | Description                                                         |
|--------------------|---------------------------------------------------------------------|
| `dnsrecon -d targeturl.com` | Standard DNS reconnaissance tool.                              |
| `dnsenum targeturl.com` | DNS enumeration tool.                                              |
| `dnsmap targeturl.com` | DNS mapping tool for discovering records.                         |

### Additional DNS Scanners & Record Enum
- `dnstracer -v targeturl.com` - Trace DNS information.
- `dnswalk targeturl.com` - Check for internal DNS consistency.
- `fierce -dns targeturl.com` - Locates IP space and hostnames via zone transfers and brute force.

## Gathering Names & Email Addresses

| Command            | Description                                                         |
|--------------------|---------------------------------------------------------------------|
| `theharvester -d targeturl.com -b google` | Gather email addresses, hosts, and subdomains via search engines. |

## Password Profiling

| Tool               | Description                                                         |
|--------------------|---------------------------------------------------------------------|
| **Common Passwords** | `/usr/share/wordlists` - Common password wordlists.                |
| **CUPP (Common User Password Profiler)** | Customize wordlists based on personal data. [CUPP GitHub](https://github.com/Mebus/cupp.git). |

## Website Password Profiling

| Command            | Description                                                         |
|--------------------|---------------------------------------------------------------------|
| `cewl -k -v targeturl.com -w cewl-output.txt` | Crawl website and create a wordlist. |

## Document Metadata

| Tool               | Description                                                         |
|--------------------|---------------------------------------------------------------------|
| `metagoofil`       | `metagoofil -d targeturl.com -t doc,pdf,xls,ppt,odp,ods,docx,xlsx,pptx -l 200 -n 50 -o foldername -f results.html` | Download documents from a site and extract metadata. |

## Route Mapping

| Command            | Description                                                         |
|--------------------|---------------------------------------------------------------------|
| `traceroute targeturl.com` | Standard route tracing tool.                                     |
| `hping3 -S targeturl.com -p 80 -c 3` | Network packet assembler/analyzer.                              |
| `intrace`          | [GitHub - intrace](https://github.com/robertswiecki/intrace) - Exploit existing TCP connections for route mapping. |

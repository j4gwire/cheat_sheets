# Basics of Cybersecurity Cheat Sheet

## Overview

### What is Information Security?
Information security focuses on the value of the information being protected rather than how it is being protected. It encompasses physical security and cybersecurity. Cybersecurity tends to focus on the security of digital systems but should not be limited to digital elements, as most attacks have human and physical factors as well.

---

## Offense: Threat Actor Groups

### What are Threat Actor Groups?
Cybersecurity professionals must understand different types of threat actor groups that vary in motivation, resources, and techniques. The five main types of cyber attacker groups are:

| Group                     | Description                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1. Script Kiddie**       | Least advanced, relies on off-the-shelf tools, and publicly available exploits. Motivated by reputation or entertainment. Usually self-taught, typically young.      |
| **2. Hacktivist**          | Motivated by ideological reasons (political, economic change). Operate at scale, with varied tools, often targeting entities they oppose.                         |
| **3. Criminal Gang**       | Fastest growing group, engaged in ransomware, extortion, and theft. Often well-funded, operate with organized infrastructure.                                      |
| **4. Nation State Hacker** | Operates on behalf of a government or intelligence agency. Uses advanced tools, employs large resources, and engages in sophisticated attacks.                     |
| **5. Malicious Insider**   | Authorized access within an organization, driven by personal or financial motivations, can steal, leak, or damage data.                                             |

---

## Offense: Types of Cyber Attacks

| Attack Type                 | Description                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Denial of Service (DoS)** | Attack that causes system outage or partial service interruption by overwhelming network traffic.                           |
| **Distributed DoS (DDoS)**  | DoS attack from multiple sources, often executed using botnets.                                                             |
| **Phishing**                | Sending fraudulent messages to steal personal information.                                                                 |
| **Spear Phishing**          | Targeted phishing using personal details gathered through research.                                                         |
| **SQL Injection**           | Exploiting vulnerabilities in databases via malicious code in SQL queries.                                                  |
| **Malware**                 | Malicious software designed to harm or exploit systems (e.g., ransomware).                                                  |
| **Man in the Middle (MitM)**| Attackers intercept communications between client and server.                                                              |
| **DNS Attack**              | Attacks targeting DNS protocols like spoofing or cache poisoning.                                                          |

---

## Offense: Structure of a Cyber Attack

### Lockheed Martin Cyber Kill Chain® Framework
1. **Reconnaissance**: Information gathering
2. **Weaponization**: Arming the payload
3. **Delivery**: Delivering the payload (via email, USB, etc.)
4. **Exploitation**: Executing code on the victim's system
5. **Installation**: Installing malware
6. **Command & Control (C2)**: Remote control of victim system
7. **Actions on Objectives**: Achieving the attacker's goal

### MITRE ATT&CK Matrix
A framework used to categorize tactics, techniques, and procedures (TTPs) used by adversaries.

---

## Offense: Funding and Profitability of Cybercrime

| Driver                     | Description                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------|
| **Activism**                | Political, ideological or social motivations behind cybercrime.                                 |
| **National Interest**       | Attacks backed by state interests, targeting other states or organizations for political gain.  |
| **Profitability**           | Financial gain from cybercrime, such as extortion, ransomware, and data theft.                  |

### Ecosystem in Action
1. Malware records keystrokes and screenshots.
2. Criminals buy email lists and distribute malware.
3. Criminals access banking logins, use money mules, and transfer cryptocurrencies.

---

## Offense: Social Engineering

### What is Social Engineering?
The manipulation of individuals to divulge confidential information. It uses psychology, biology, and manipulation tactics to exploit human weaknesses.

### Examples of Social Engineering Tactics:
- Scams and confidence tricks
- Tailgating or closely following individuals for access
- Get-rich-quick schemes

### Why Social Engineering Works:
- Humans are prone to irrational and flawed decision-making.
- Attackers exploit short-term gratification, fear, or stress.

### Defense Against Social Engineering:
- Be aware of common tactics.
- Challenge unusual requests.
- Verify suspicious emails and sources.

---

## Offense: OSINT (Open Source Intelligence)

### What is OSINT?
Intelligence gathering using publicly available information (e.g., websites, social media).

### Benefits of OSINT:
- Low cost, easy to acquire.
- Undetectable by the target.

### Sources of Open Information:
- Company websites
- Media and news sources
- Social media
- Public government records

---

## Offense: Technical Scanning

### What is Technical Scanning?
Techniques used to collect information about networks during reconnaissance.

| Technique            | Description                                                                                        |
|----------------------|----------------------------------------------------------------------------------------------------|
| **Ping Test**        | Sends an ICMP packet to check if a machine is active and reachable.                                |
| **Traceroute**       | Maps network path and identifies routers between client and server.                                |
| **Port Scanning**    | Scans for open ports to detect vulnerable services.                                                |
| **Network Vulnerability Scanning** | Detects and exploits known vulnerabilities on a network.                                      |

---

## Offense: Case Studies

| Case Study           | Description                                                                                        |
|----------------------|----------------------------------------------------------------------------------------------------|
| **Stuxnet**          | A highly targeted malware that disrupted Iranian uranium processing facilities.                   |
| **Equifax**          | Data breach compromising sensitive personal data of over 147 million people.                       |
| **NSA Leaks (Snowden)** | Leaks by Edward Snowden exposing classified government surveillance.                              |
| **SolarWinds**       | Supply chain attack exploiting trusted software updates, impacting thousands of organizations.      |

---

## Defense: Financial Impacts

### Financial Impact of Cyber Attacks
- Average global cost of a data breach: $4.35M
- Regulatory fines, lost business, and remediation costs can have a significant impact.

---

## Defense: Security Strategy

### Security Maturity Levels (PRISMA)
| Level | Description                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------|
| **1. Policies**    | Documented policies to assess risk, implement controls, and monitor effectiveness.                             |
| **2. Procedures**  | Formal, documented procedures for security controls and IT security responsibilities.                          |
| **3. Implementation** | Procedures communicated and consistently implemented through training.                                       |
| **4. Test**        | Regular tests to evaluate security controls and implement corrective actions based on incidents.              |
| **5. Integration** | Full integration of security into organizational culture and decision-making, with ongoing threat assessment. |

### 10 Steps to Cybersecurity
1. Risk management
2. Engagement and training
3. Asset management
4. Architecture and configuration
5. Vulnerability management
6. Identity and access management
7. Data security
8. Logging and monitoring
9. Incident management
10. Supply chain security

---

## Defense: Security Market

Large organizations typically use products from various cybersecurity vendors. This ecosystem is supported by authorities, charities, and government entities to enhance organizational security.

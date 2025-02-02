# Web Development Cheat Sheet

## Web App Security Browser Isolation

| Attack Mode | Description |
|-------------|-------------|
| **Attack the connection** | Steal password, hijack existing connection |
| **Attack the server** | Inject code to cause damage |
| **Attack the browser** | Inject code to cause damage |
| **Breach the browser, attack client** | Fool user (phishing) |

### Security Defenses
| Defense | Description |
|----------|-------------|
| **Isolation in browsers** | Web apps run in isolated sandbox |
| **Cryptography** | Encrypt sensitive data |

## Same-Origin Policy

| Concept | Description |
|---------|-------------|
| **General Idea** | Separate content with different trust levels, restrict communication between frames |
| **Origin** | Protocol, Domain, Port |
| **Access** | DOM resources, cookies, AJAX requests |

### When Same-Origin Policy is too Restrictive
| Scenario | Description |
|----------|-------------|
| **Subdomains** | Useful for frames with different origins to communicate within the same organization |
| **Web fonts / CDN** | Allow communication for specific use cases |

### HTML5 Features
| Feature | Description |
|---------|-------------|
| **Access-Control-Allow-Origin** | Allows cross-origin access |
| **HTML5 postMessage** | Safe messaging between domains |

## JavaScript Framework Criticisms

| Issue | Description |
|-------|-------------|
| **Angular** | Digest cycle overheads, large data tables, slow DOM access, mobile problems |
| **Node.js** | Callback hell, concurrency support issues |

## Network Security

| Attack Type | Description |
|-------------|-------------|
| **Man in the Middle (MITM)** | Attacker intercepts network communication |
| **Passive Attacks** | Eavesdrop on network traffic |
| **Active Attacks** | Inject, modify, reorder, or block packets |

### SSL/TLS (HTTPS)
| Issue | Description |
|-------|-------------|
| **SSL Problems** | Server pages with HTTPS links altered to HTTP, mixed content risks |
| **SSL/TLS** | Protocol for secure communication between browser and server |

### Session Attacks

| Attack | Description |
|--------|-------------|
| **Session ID** | Session IDs must be unpredictable and use HTTPS for cookie protection |
| **CSRF** | Prevent POST submissions directly from external forms |

## Code Injection Attacks

| Attack | Description |
|--------|-------------|
| **XSS (Cross-Site Scripting)** | Injecting malicious code into a webpage |
| **Stored XSS** | Malicious script stored on the server and executed when loaded |
| **Reflected XSS** | Script reflected immediately back to the client |

## Phishing and Social Engineering

| Attack | Description |
|--------|-------------|
| **Phishing** | Trick users into revealing personal information |
| **Spear Phishing** | Phishing with personalized information |

## Denial of Service (DoS) Attacks

| Attack | Description |
|--------|-------------|
| **DoS** | Overload server resources to disrupt service |
| **Countermeasures** | Rate limiting, resource quotas, and pricing strategies |

## Large-Scale Web Applications

| Concept | Description |
|---------|-------------|
| **Scale-Out Architecture** | Add/remove instances to scale the application |
| **Load Balancing** | Distribute traffic across servers for better performance |
| **Data Sharding** | Spread data across multiple instances for better scaling and failure tolerance |

### Other Considerations
| Concept | Description |
|---------|-------------|
| **Content Delivery Network (CDN)** | Use distributed servers for fast delivery of static content |
| **Memcache** | In-memory caching system for fast access to frequently requested data |


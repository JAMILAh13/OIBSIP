# Research Report on Common Network Security Threats

## 1. Introduction

Network security threats are malicious activities that target computer networks, devices, servers, applications, and users. These threats can interrupt services, steal sensitive information, redirect users to fake websites, or allow attackers to secretly monitor communications.

This report focuses on three common network security threats:

1. Denial-of-Service (DoS) and Distributed Denial-of-Service (DDoS) attacks
2. Man-in-the-Middle (MITM) attacks
3. Spoofing attacks

For each threat, this report explains how it works, its impact, real-world examples, and possible mitigation methods.

---

## 2. Denial-of-Service (DoS) and Distributed Denial-of-Service (DDoS) Attacks

### 2.1 What is a DoS attack?

A Denial-of-Service attack is an attack where a cybercriminal attempts to make a system, website, server, or network unavailable to legitimate users. This is usually done by overwhelming the target with too much traffic or too many requests.

A Distributed Denial-of-Service attack is a larger version of a DoS attack. Instead of using one device, the attacker uses many compromised devices, often called a botnet, to attack the target at the same time.

### 2.2 How DoS and DDoS attacks work

A DoS or DDoS attack usually works by flooding a target system with traffic until it cannot respond properly. The target may slow down, crash, or become completely unavailable.

Common types include:

- **Volumetric attacks:** Flood the network with huge amounts of traffic.
- **Protocol attacks:** Abuse network protocols to consume server or firewall resources.
- **Application-layer attacks:** Target web applications by sending many requests that look normal but overload the application.

In a DDoS attack, attackers often use infected devices such as routers, cameras, computers, and Internet of Things devices. These compromised devices are controlled remotely and used to send traffic to the victim.

### 2.3 Impact of DoS and DDoS attacks

DoS and DDoS attacks can cause:

- Website or service downtime
- Loss of customers and revenue
- Damage to an organisation’s reputation
- Increased recovery and security costs
- Disruption of business operations
- Possible distraction while attackers attempt other attacks

### 2.4 Real-world example

In 2024, Cloudflare reported mitigating a record-breaking DDoS attack that peaked at 5.6 Tbps. The attack was linked to a Mirai-variant botnet and targeted an internet service provider. Cloudflare also reported that it mitigated 6.9 million DDoS attacks in the fourth quarter of 2024 alone.

This example shows how large DDoS attacks have become and how attackers often use compromised IoT devices to generate massive amounts of traffic.

### 2.5 Mitigation and prevention

Organisations can reduce the risk of DoS and DDoS attacks by:

- Using DDoS protection services
- Configuring firewalls and intrusion prevention systems
- Applying rate limiting to control excessive requests
- Using load balancers to distribute traffic
- Monitoring network traffic for unusual spikes
- Keeping systems and IoT devices updated
- Blocking traffic from suspicious sources
- Creating an incident response plan

---

## 3. Man-in-the-Middle (MITM) Attacks

### 3.1 What is a MITM attack?

A Man-in-the-Middle attack happens when an attacker secretly places themselves between two communicating parties. The attacker can intercept, read, modify, or redirect information without the users realising.

For example, a user may think they are communicating directly with a website, but the attacker is silently intercepting the connection.

### 3.2 How MITM attacks work

MITM attacks can happen in different ways, including:

- **Public Wi-Fi interception:** Attackers monitor insecure public Wi-Fi networks.
- **ARP spoofing:** Attackers send fake Address Resolution Protocol messages on a local network.
- **DNS spoofing:** Attackers redirect users to fake websites.
- **HTTPS stripping:** Attackers attempt to downgrade secure HTTPS connections to insecure HTTP.
- **Session hijacking:** Attackers steal session cookies to access user accounts.

In a typical MITM attack, the attacker first intercepts the communication. Then they may capture usernames, passwords, banking details, or other sensitive information. In some cases, they may also alter messages or redirect users to malicious websites.

### 3.3 Impact of MITM attacks

MITM attacks can lead to:

- Theft of login credentials
- Financial fraud
- Identity theft
- Unauthorised access to accounts
- Data manipulation
- Loss of confidentiality and trust
- Compromise of business communication

### 3.4 Real-world example

MITM-style attacks are commonly seen in phishing and fake Wi-Fi scenarios. Attackers may create a fake Wi-Fi hotspot that looks legitimate. When victims connect, the attacker can monitor their traffic or redirect them to fake login pages.

Another related example is session hijacking, where attackers steal authentication tokens or cookies. In 2023, Microsoft reported that the Storm-0558 threat actor used forged authentication tokens to access customer email accounts. While this specific incident involved token forgery rather than a basic Wi-Fi MITM attack, it demonstrates the serious risk of attackers gaining access to authentication material.

### 3.5 Mitigation and prevention

Users and organisations can reduce MITM risk by:

- Using HTTPS websites only
- Avoiding sensitive logins on public Wi-Fi
- Using a trusted VPN on public networks
- Enabling multi-factor authentication
- Avoiding unknown or suspicious Wi-Fi networks
- Keeping browsers and operating systems updated
- Using secure email and messaging protocols
- Implementing certificate validation
- Using network monitoring tools to detect unusual traffic
- Educating users about phishing and fake login pages

---

## 4. Spoofing Attacks

### 4.1 What is spoofing?

Spoofing is when an attacker disguises themselves as a trusted device, user, website, or service. The goal is to trick systems or people into trusting the attacker.

Spoofing is often used to support other attacks, such as MITM attacks, phishing, malware delivery, and unauthorised access.

### 4.2 Types of spoofing

Common spoofing attacks include:

#### IP spoofing

The attacker changes the source IP address in packets to make traffic appear as if it comes from a trusted source.

#### ARP spoofing

The attacker sends fake ARP messages on a local network. This can link the attacker’s MAC address to the IP address of a trusted device, such as a router. Traffic can then be redirected through the attacker’s device.

#### DNS spoofing

The attacker manipulates DNS records or DNS cache entries so that users are redirected to fake websites even when they type the correct domain name.

#### Email spoofing

The attacker sends emails that appear to come from a trusted sender. This is commonly used in phishing attacks.

#### Website spoofing

The attacker creates a fake website that looks like a real one to steal usernames, passwords, or payment information.

### 4.3 How spoofing works

Spoofing works by abusing trust. Networks and users often trust certain addresses, names, or identities. Attackers take advantage of this by pretending to be something legitimate.

For example, in DNS spoofing, a user may type a real website address, but the DNS response sends them to the attacker’s fake website. The user may not immediately notice because the fake site can look very similar to the real one.

### 4.4 Impact of spoofing attacks

Spoofing can cause:

- Credential theft
- Malware infections
- Data interception
- Unauthorised network access
- Financial loss
- Brand and reputation damage
- Redirection to malicious websites
- Business email compromise

### 4.5 Real-world example

DNS spoofing and DNS cache poisoning attacks have been used to redirect users from legitimate websites to malicious ones. Attackers insert false DNS records into a DNS cache, causing users to be sent to the wrong IP address.

Email spoofing is also widely used in phishing campaigns. Attackers may send emails that look like they come from a bank, employer, school, or service provider to trick users into clicking malicious links.

### 4.6 Mitigation and prevention

Spoofing can be reduced by:

- Using DNSSEC to help verify DNS responses
- Configuring email authentication such as SPF, DKIM, and DMARC
- Using static ARP entries for critical systems where appropriate
- Enabling Dynamic ARP Inspection on managed switches
- Using strong firewall rules
- Monitoring for unusual ARP or DNS activity
- Training users to check email senders and website URLs carefully
- Using multi-factor authentication
- Keeping systems updated
- Avoiding clicking suspicious links

---

## 5. Preventive Security Measures Across All Threats

Although each threat works differently, many general security practices help protect networks from multiple types of attacks.

### 5.1 Network monitoring

Organisations should monitor network traffic to detect unusual patterns, such as traffic spikes, unknown devices, or suspicious DNS activity.

### 5.2 Regular updates and patching

Operating systems, routers, firewalls, applications, and IoT devices should be updated regularly to fix known vulnerabilities.

### 5.3 Strong authentication

Multi-factor authentication should be used to reduce the risk of account compromise, especially if passwords are stolen.

### 5.4 Secure network configuration

Firewalls, routers, and switches should be configured securely. Unused ports and services should be disabled.

### 5.5 User awareness training

Many attacks rely on tricking users. Training can help users recognise phishing emails, fake websites, suspicious links, and unsafe Wi-Fi networks.

### 5.6 Incident response planning

Organisations should have a clear response plan that explains what to do during a cyberattack. This includes identifying the attack, containing it, recovering systems, and reporting the incident.

---

## 6. Comparison Table

| Threat | How it Works | Main Impact | Mitigation |
|---|---|---|---|
| DoS/DDoS | Floods a system with traffic or requests | Downtime, service disruption, financial loss | DDoS protection, rate limiting, firewalls, monitoring |
| MITM | Intercepts communication between two parties | Credential theft, data interception, session hijacking | HTTPS, VPN, MFA, certificate validation, secure Wi-Fi |
| Spoofing | Pretends to be a trusted identity, device, or service | Phishing, redirection, unauthorised access | DNSSEC, SPF/DKIM/DMARC, ARP protection, user training |

---

## 7. Conclusion

DoS/DDoS, MITM, and spoofing attacks are common network security threats that can seriously affect individuals and organisations. DoS and DDoS attacks mainly target availability by overwhelming systems. MITM attacks target confidentiality and integrity by intercepting communication. Spoofing attacks abuse trust by pretending to be a legitimate source.

The best defence is a layered security approach. This includes technical controls such as firewalls, DDoS protection, encryption, DNSSEC, email authentication, and network monitoring. It also includes good security habits such as user awareness, regular updates, strong passwords, and multi-factor authentication.

By understanding how these attacks work and applying preventive measures, organisations can reduce risk and improve their overall network security posture.

---

## 8. References

- Cloudflare. “Record-breaking 5.6 Tbps DDoS attack and global DDoS trends for 2024 Q4.” Published 21 January 2025.
- Microsoft Security. “Analysis of Storm-0558 techniques for unauthorized email access.” Published 14 July 2023.
- Rapid7. “What is a Man-in-the-Middle Attack?”
- Splunk. “What Is a MITM Attack? Man-in-the-Middle Attacks, Explained.”
- NordLayer. “What Is DNS Spoofing? DNS Cache Poisoning Attack.”

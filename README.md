# Network Traffic Analysis with Wireshark

## Project Overview

This project demonstrates the analysis of network traffic using Wireshark in order to identify protocols, inspect communications, and detect potential security risks within a public network environment.

## Objectives

- Capture live network traffic.
- Identify common network protocols.
- Analyze conversations and packet flows.
- Detect suspicious or insecure communications.
- Document findings and recommendations.

---

## Tools Used

- Wireshark
- Kali Linux
- Public Wi-Fi Network

---

## Protocols Identified

| Protocol | Purpose |
|-----------|----------|
| HTTP | Unencrypted web traffic |
| HTTPS | Secure web traffic |
| DNS | Domain name resolution |
| ARP | Address Resolution Protocol |
| ICMP | Network diagnostics |
| TCP | Reliable transport protocol |
| UDP | Connectionless transport protocol |

---

## Wireshark Filters Used

### HTTP Traffic

```wireshark
http
```

### HTTPS Traffic

```wireshark
tls
```

### DNS Queries

```wireshark
dns
```

### ARP Traffic

```wireshark
arp
```

### ICMP Packets

```wireshark
icmp
```

### TCP Traffic

```wireshark
tcp
```

### UDP Traffic

```wireshark
udp
```

### Traffic from a Specific IP

```wireshark
ip.addr == 192.168.1.100
```

---

## Sample Findings

### DNS Activity

Observed multiple DNS requests to external resolvers.

Examples:

- google.com
- youtube.com
- facebook.com
- microsoft.com

Finding:
DNS traffic can reveal browsing activity even when HTTPS is used.

---

### HTTP Traffic

Observed unencrypted HTTP requests.

Risk:
Data transmitted through HTTP can be intercepted by attackers performing packet sniffing.

---

### HTTPS Traffic

TLS encrypted sessions were identified.

Finding:
Traffic contents were protected, but metadata such as destination IP addresses and domains remained visible.

---

### ARP Activity

Several ARP requests and responses were detected.

Finding:
Normal network behavior was observed.

Potential Risk:
ARP spoofing attacks could be possible in public networks if protections are not implemented.

---

### ICMP Traffic

ICMP Echo Requests and Echo Replies were captured.

Examples:

- Ping tests to external hosts.
- Network reachability verification.

---

## Security Risks Identified

### 1. Unencrypted Communications

Risk Level: Medium

HTTP traffic may expose:

- Credentials
- Session tokens
- User activity

Recommendation:

- Use HTTPS exclusively.

---

### 2. Information Disclosure Through DNS

Risk Level: Low

DNS requests reveal visited domains.

Recommendation:

- Use encrypted DNS services (DoH / DoT).

---

### 3. ARP Spoofing Possibility

Risk Level: Medium

Public networks are vulnerable to ARP poisoning attacks.

Recommendation:

- Use VPN connections on public Wi-Fi.

---

## Key Evidence Collected

- Protocol Statistics
- Packet Details
- DNS Requests
- HTTP Sessions
- TCP Conversations
- Endpoint Analysis

---

## Skills Demonstrated

- Packet Analysis
- Protocol Identification
- Network Monitoring
- Threat Detection
- Traffic Investigation
- Security Assessment

---

## Conclusion

The analysis successfully identified common network protocols and demonstrated how network traffic can reveal valuable information about user activity. The project highlights the importance of encrypted communications and secure network practices when using public networks.
---

## Key Learning Outcomes

This project strengthened my understanding of network communications, packet analysis techniques, and the role of traffic monitoring in cybersecurity operations and incident detection.

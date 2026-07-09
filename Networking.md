# Networking Basics

## OSI Model

| Layer | Name | Function |
|---|---|---|
| 7 | Application | End-user services (HTTP, FTP, DNS) |
| 6 | Presentation | Data translation, encryption, compression |
| 5 | Session | Manages sessions between applications |
| 4 | Transport | End-to-end delivery (TCP, UDP) |
| 3 | Network | Logical addressing and routing (IP) |
| 2 | Data Link | Physical addressing (MAC), switches |
| 1 | Physical | Cables, signals, hardware transmission |

---

## TCP/IP Model

| Layer | Maps to OSI |
|---|---|
| Application | Application, Presentation, Session |
| Transport | Transport |
| Internet | Network |
| Network Access | Data Link, Physical |

---

## HTTP vs HTTPS

### HTTP
- Port 80
- Data transmitted in plaintext
- Vulnerable to interception (as demonstrated with Burp Suite in this lab)

### HTTPS
- Port 443
- Data encrypted using TLS/SSL
- Protects confidentiality and integrity of data in transit

---

## Lab Network Configuration

| Setting | Value |
|---|---|
| Kali Linux IP | 192.168.56.102 |
| Metasploitable2 IP | 192.168.56.101 |
| Adapter Type | Host-Only (isolated lab network) |
| Secondary Adapter | NAT (for internet access on Kali) |

**Connectivity Test:**
```bash
ping 192.168.56.101
```
Confirmed successful ICMP Echo Request/Reply exchange between Kali and Metasploitable2, verified via Wireshark packet capture.

---

## Nmap Scanning

```bash
nmap 192.168.56.101
```
Used to enumerate open ports and running services on the Metasploitable2 target, forming the basis for identifying attack surface in later tasks.

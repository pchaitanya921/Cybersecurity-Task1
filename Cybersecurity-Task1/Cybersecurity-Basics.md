# Cybersecurity Basics

## The CIA Triad

The CIA Triad is the foundational model for information security, made up of three core principles:

### Confidentiality
Ensures that information is accessible only to authorized individuals.
- Example controls: encryption, access control lists, authentication

### Integrity
Ensures that information remains accurate and unaltered except by authorized action.
- Example controls: hashing (SHA-256), checksums, digital signatures

### Availability
Ensures that information and systems are accessible to authorized users when needed.
- Example controls: redundancy, backups, DDoS protection

---

## Common Threats

### Phishing
Social engineering attack where attackers impersonate trusted entities (email, SMS, or web) to trick users into revealing credentials or installing malware.

### Malware
Malicious software designed to damage, disrupt, or gain unauthorized access to systems. Categories include viruses, worms, trojans, ransomware, and spyware.

### SQL Injection
A web application vulnerability where an attacker injects malicious SQL statements through input fields to manipulate or extract database contents.

### Cross-Site Scripting (XSS)
Injection of malicious scripts into trusted websites, executed in a victim's browser to steal cookies, sessions, or perform actions on their behalf.

### Distributed Denial of Service (DDoS)
An attack that floods a target system with traffic from multiple sources, overwhelming its resources and making services unavailable to legitimate users.

### Man-in-the-Middle (MitM)
An attacker secretly intercepts and possibly alters communication between two parties who believe they are communicating directly with each other.

---

## Lab Setup Summary

For this task, a two-machine lab was built:

1. **Kali Linux** – used as the attacker/analysis machine, running Nmap, Wireshark, Burp Suite, Netcat, and OpenSSL.
2. **Metasploitable2** – an intentionally vulnerable Linux VM used as the target for scanning, traffic capture, and analysis.

Both machines were connected via a **Host-Only Adapter** in VirtualBox to isolate lab traffic from the external network, while Kali also retained a **NAT adapter** for internet access (updates, tool installation).

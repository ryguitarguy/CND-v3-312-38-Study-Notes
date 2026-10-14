# Volume 1: Certified Network Defender (CND v3) Study Notes

---

## Module 01: Network Attacks and Defense Fundamentals

### 1. Information Assurance (IA) Principles
Network security rests on the traditional **CIA Triad**, which CND expands with two additional pillars[cite: 1]:
* **Confidentiality:** Ensuring data is accessible only to authorized entities[cite: 1].
* **Integrity:** Safeguarding the accuracy and completeness of information[cite: 1].
* **Availability:** Ensuring timely and reliable access to data and services[cite: 1].
* **Authentication:** Verifying the identity of users or systems[cite: 1].
* **Non-repudiation:** Guaranteeing that a sender cannot deny authenticating an action[cite: 1].

### 2. Threats, Vulnerabilities, and Risk
* **Threat Sources:**
  * **Natural:** Floods, earthquakes[cite: 1].
  * **Unintentional:** Accidental deletion, misconfigurations[cite: 1].
  * **Intentional:** Targeted cyberattacks (Internal or External)[cite: 1, 13].
* **Threat Actors:**
  * **Script Kiddies:** Novice attackers relying on pre-written tools without deep technical understanding[cite: 2].
  * **Hacktivists:** Motivated by political, social, or ideological agendas[cite: 2].
  * **Insider Threats:** Current or former employees with legitimate access who misuse privileges intentionally or carelessly[cite: 2].
  * **Organized Cybercriminals & Industrial Spies:** Financial- or intelligence-driven entities targeting high-value assets[cite: 2].
  * **State-Sponsored Hackers:** Highly trained, patient attackers targeting critical infrastructure and government entities[cite: 2].
* **Core Definitions:**
  * **Vulnerability:** A flaw in design, implementation, configuration, or security policy[cite: 2].
  * **Security Incident:** Occurs when a threat actor leverages a technique to exploit a vulnerability[cite: 2].
  * **Risk:** Potential loss resulting from a threat exploiting a vulnerability, evaluated via a **Risk Matrix** ($\text{Probability} \times \text{Impact}$)[cite: 2].

### 3. Network-Level Attack Techniques (TTPs)
* **Reconnaissance:** DNS Footprinting, Network Sniffing, and Port Scanning to map open ports and running services[cite: 2].
* **Man-in-the-Middle (MitM):** Intercepting and altering traffic between two communicating hosts without their knowledge[cite: 2].
* **Password Exploitation:**
  * **Dictionary Attack:** Iterating through lists of common words[cite: 2].
  * **Brute Force Attack:** Systematically trying every possible character combination[cite: 2].
  * **Hybrid Attack:** Combining dictionary words with numbers or symbols[cite: 2].
  * **Rainbow Table Attack:** Using precomputed tables of cryptographic hashes to rapidly reverse password functions[cite: 2].
  * **Birthday Attack:** Exploiting mathematical probability in hash functions to find collision pairs[cite: 2].
* **Layer 2 Infrastructure Attacks:**
  * **ARP Poisoning:** Sending forged ARP messages to link an attacker's MAC address with the IP of a legitimate default gateway[cite: 2].
  * **DHCP Starvation & Spoofing:** Flooding a DHCP server with fake MAC addresses to exhaust available IPs (Starvation), then deploying a rogue DHCP server (Spoofing) to redirect traffic[cite: 2].
  * **Switch Port Stealing & MAC Duplicating:** Flooding switch binding tables to force hub-like behavior, broadcasting unicast traffic across all physical ports[cite: 2].
* **DoS & DDoS:** Overwhelming target compute resources or bandwidth to crash services[cite: 3].

### 4. Modern Defense Strategies
* **Continual/Adaptive Security Strategy:** Cycles continuously through four operational phases[cite: 3]:
  1. **Protect:** Implement baseline safeguards to resist attacks[cite: 3].
  2. **Detect:** Monitor network activity to identify active intrusions[cite: 3].
  3. **Respond:** Contain threats and isolate compromised endpoints immediately[cite: 3].
  4. **Predict:** Utilize threat intelligence to anticipate incoming attack vectors[cite: 3].
* **Defense-in-Depth (Multi-Layered Security):** Places redundant controls across **People** (training), **Operations** (incident response policies), and **Technology** (firewalls, encryption) so if one layer fails, subsequent layers prevent a total breach[cite: 3].

---

## Module 02: Administrative Network Security and Governance

### 1. Regulatory Frameworks and Compliance
* Requires implementing documented security controls and undergoing regular internal and external audits[cite: 3].
* Driven by cybersecurity frameworks that define baseline requirements for risk management, access management, and breach notification[cite: 3].

### 2. Security Policy Engineering Lifecycle
A **Security Policy** is a formal, high-level document defining security goals, acceptable behaviors, and baseline protection requirements[cite: 4]:
1. **Design & Development:** Defining mandatory rules for acceptable use, password complexity, remote work access, data classification, and incident management[cite: 4].
2. **Enforcement & Oversight:** Implementing technical controls that enforce policy rules automatically (e.g., Active Directory Group Policies)[cite: 4].
3. **Review & Maintenance:** Periodically updating guidelines for emerging technologies and newly discovered threats[cite: 4].

### 3. IT Asset Management (ITAM)
* **Real-Time Inventories:** Categorize hardware, software, and network devices by IP address, MAC address, operational owner, and physical location[cite: 4].
* **Security Baseline Configurations:** Ensure every newly deployed system meets minimum security hardening standards before entering production[cite: 4].
* **Lifecycle Tracking:** Manage assets from acquisition and maintenance through safe **Data Destruction** and hardware retirement[cite: 4].

### 4. Security Awareness and Trend Intelligence
* **Awareness Training:** Mitigates human error and builds a security culture against social engineering (phishing, pretexting)[cite: 4].
* **Trend Intelligence:** Tracking cybersecurity news feeds, industry research, technical webinars, threat reports, and vulnerability databases[cite: 4].

---

## Module 03: Technical Network Security Controls and Protocols

### 1. Access Control Models
Access control governs how a **subject** interacts with an **object**[cite: 5]:

| Model | Core Mechanism |
| :--- | :--- |
| **Discretionary Access Control (DAC)** | The asset owner explicitly sets permission levels for other users[cite: 5]. |
| **Mandatory Access Control (MAC)** | Centralized security authority grants access based on formal security classifications and clearances[cite: 5]. |
| **Role-Based Access Control (RBAC)** | Permissions are assigned to organizational roles rather than individual user accounts[cite: 5]. |
| **Identity & Access Management (IAM)** | Centralized framework for identity verification, provisioning, MFA authentication, and authorization[cite: 5]. |

### 2. Cryptographic Primitives
* **Secure Hashing Algorithms (SHA):** Functions (like SHA-2 and SHA-3) that generate a fixed-size mathematical signature from variable-length data to verify **Data Integrity**[cite: 5].
* **Hash-based Message Authentication Code (HMAC):** Combines a cryptographic hash function with a secret shared key to provide both **data integrity** and **message authentication**[cite: 5].

### 3. Network Segmentation & DMZ
* **Segmentation:** Divides a network into isolated zones to prevent lateral movement[cite: 5].
* **Demilitarized Zone (DMZ):** A physical or logical subnet separating the internal private network from untrusted public networks[cite: 5]. Hosts public-facing services (Web, DNS, Email servers) so a compromised public server cannot directly access internal workstations, databases, or domain controllers[cite: 5, 6].

```text
[ UNTRUSTED INTERNET ] 
          │
     [ Firewall ]
          │
          ├───► [ Demilitarized Zone (DMZ) ] (Web, DNS, Email Servers)
          │
     [ Firewall ]
          │
[ SECURE INTERNAL NETWORK ] (Workstations, Databases, Domain Controllers)
```
[cite: 6]

### 4. Core Network Security Protocols
* **S/MIME vs. PGP (Email Security):**
  * **S/MIME:** Uses a centralized Public Key Infrastructure (PKI) with CA-signed X.509 certificates[cite: 6].
  * **PGP:** Relies on a decentralized "Web of Trust"[cite: 6].
* **HTTPS & TLS:** Operates above the transport layer (TCP Port 443) to encrypt HTTP web traffic using asymmetric cryptography for key exchange and symmetric encryption for data transfer[cite: 6].
* **IPsec (OSI Layer 3 Network Layer Security):**
  * **Authentication Header (AH):** Provides connectionless integrity and data origin authentication, but **no encryption/confidentiality**[cite: 6].
  * **Encapsulating Security Payload (ESP):** Provides confidentiality (encryption), data origin authentication, and integrity[cite: 6].
  * **Transport Mode:** Encrypts only the IP payload while leaving the original IP header intact (used for host-to-host communications)[cite: 6].
  * **Tunnel Mode:** Encrypts the entire original IP packet (header + payload) and encapsulates it in a new IP header (used for Site-to-Site VPNs)[cite: 6].

---

## Module 04: Network Perimeter Security and Defense Architecture

### 1. Firewall Technologies
| Firewall Type | OSI Layer | Operational Mechanism |
| :--- | :--- | :--- |
| **Packet Filtering** | Layer 3 & 4 | Inspects headers (Source/Dest IP, port, protocol) without tracking connection state[cite: 7]. |
| **Circuit-Level Gateway** | Layer 5 | Validates session establishment handshakes (e.g., TCP 3-way handshake)[cite: 7]. |
| **Application-Level / Proxy** | Layer 7 | Inspects actual application payload data (e.g., blocking malicious HTTP GET requests)[cite: 7]. |
| **Stateful Multilayer Inspection** | Layers 3–4+ | Combines header analysis with active connection state tables to match established sessions[cite: 7]. |
| **Next-Generation Firewall (NGFW)** | Multi-Layer | Integrates stateful inspection with Deep Packet Inspection (DPI), inline IPS, threat intelligence, and user/application visibility[cite: 7]. |

### 2. Intrusion Detection and Prevention Systems (IDS/IPS)
* **IDS vs. IPS:** An **IDS** analyzes deep traffic behavior to alert administrators to malicious events, whereas an **IPS** sits directly **inline** to actively drop malicious packets automatically[cite: 7].
* **Deployment Scopes:**
  * **Network-Based IDS (NIDS):** Deployed at choke points (e.g., switch SPAN/TAP ports) to monitor subnet traffic[cite: 8].
  * **Host-Based IDS (HIDS):** Installed directly on endpoints to monitor system calls, local logs, registry changes, and file integrity[cite: 8].
* **Open-Source Tools:**
  * **Snort:** Signature-based NIDS engine[cite: 8].
  * **Suricata:** Multi-threaded NIDS/IPS engine[cite: 8].
  * **Zeek (formerly Bro):** Network analysis framework often paired with ELK logging stacks[cite: 8, 13].
  * **OSSEC / Wazuh:** Host inspection and telemetry frameworks[cite: 8].
* **Tuning Metrics:**
  * **False Positive:** Benign traffic incorrectly flagged as malicious[cite: 8].
  * **False Negative:** Actual malicious traffic missed by detection rules[cite: 8].

### 3. Router and Switch Security Hardening
* Disable unused physical switch ports and assign them to an isolated, unused VLAN[cite: 8].
* Enable **Port Security** to limit the maximum number of MAC addresses learned on a switch port[cite: 8].
* Implement **DHCP Snooping** to block untrusted DHCP server messages[cite: 8].
* Pair with **Dynamic ARP Inspection (DAI)** to neutralize ARP poisoning[cite: 8].
* Harden the management plane: disable Telnet and HTTP in favor of **SSHv2** and **HTTPS**, and enforce strong **AAA authentication**[cite: 8].

### 4. Zero Trust & Software-Defined Perimeter (SDP)
* **Zero Trust Principle:** *"Never Trust, Always Verify"*—removes implicit trust for devices inside the network perimeter[cite: 8].
* **Software-Defined Perimeter (SDP):** Creates dynamic, temporary, one-to-one encrypted connections between an authorized endpoint and a specific application, turning protected servers into **"dark hosts"** hidden from internet scanners[cite: 8, 9].
* **Three Core SDP Components:**
  1. **SDP Controller:** Central authority that authenticates users/devices, determines permissions, and issues trust tokens[cite: 9].
  2. **SDP Initiating Host (IH):** Client device requesting access to a network resource[cite: 9].
  3. **SDP Accepting Host (AH):** Protected asset that accepts connections only after explicit authorization from the SDP Controller[cite: 9].

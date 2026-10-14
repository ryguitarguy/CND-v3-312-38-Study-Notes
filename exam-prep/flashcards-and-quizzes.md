# 🧠 CND v3 (312-38) Flashcards & Practice Quiz

Use this interactive study guide for active recall before taking practice exams[cite: 12]. Click on any flashcard or quiz question below to reveal the answer and detailed explanation[cite: 12].

---

## 🗂️ Part 1: Volume 1 Interactive Flashcards

### Module 01: Network Attacks and Defense Fundamentals

<details>
<summary><b>📇 Flashcard 1: How does CND expand the traditional CIA Triad of Information Assurance (IA)?</b></summary>
<br>
<b>Answer:</b><br>
Alongside <b>Confidentiality</b> (authorized access only), <b>Integrity</b> (accuracy and completeness), and <b>Availability</b> (timely and reliable access), CND adds[cite: 1]:
<ul>
  <li><b>Authentication:</b> Verifying the identity of users or systems[cite: 1].</li>
  <li><b>Non-repudiation:</b> Guaranteeing that a sender cannot deny authenticating an action[cite: 1].</li>
</ul>
</details>

<details>
<summary><b>📇 Flashcard 2: What is the difference between a Vulnerability, a Security Incident, and Risk?</b></summary>
<br>
<b>Answer:</b>
<ul>
  <li><b>Vulnerability:</b> A flaw in design, implementation, configuration, or security policy[cite: 2].</li>
  <li><b>Security Incident:</b> Occurs when a threat actor leverages a technique to exploit a vulnerability[cite: 2].</li>
  <li><b>Risk:</b> The potential loss resulting from a threat exploiting a vulnerability, calculated using a <b>Risk Matrix</b> that evaluates <b>Probability</b> of occurrence against severity of <b>Impact</b>[cite: 2].</li>
</ul>
</details>

<details>
<summary><b>📇 Flashcard 3: Compare the 5 Password Exploitation Techniques covered in Module 1.</b></summary>
<br>
<b>Answer:</b>
<ul>
  <li><b>Dictionary Attack:</b> Iterating through lists of common words[cite: 2].</li>
  <li><b>Brute Force Attack:</b> Systematically trying every possible character combination[cite: 2].</li>
  <li><b>Hybrid Attack:</b> Combining dictionary words with numbers or symbols[cite: 2].</li>
  <li><b>Rainbow Table Attack:</b> Utilizing precomputed tables of cryptographic hashes to reverse password functions rapidly[cite: 2].</li>
  <li><b>Birthday Attack:</b> Exploiting mathematical probability in hash functions to find collision pairs[cite: 2].</li>
</ul>
</details>

<details>
<summary><b>📇 Flashcard 4: How do DHCP Starvation and DHCP Spoofing work together in a Layer 2 attack?</b></summary>
<br>
<b>Answer:</b><br>
First, the attacker floods the network's legitimate DHCP server with fake MAC addresses to exhaust all available IP addresses (<b>DHCP Starvation</b>)[cite: 2]. Once the legitimate server cannot issue leases, the attacker sets up a rogue DHCP server (<b>DHCP Spoofing</b>) to hand out malicious gateway/DNS configurations that redirect host traffic[cite: 2].
</details>

<details>
<summary><b>📇 Flashcard 5: What are the 4 operational phases of the Continual/Adaptive Security Strategy, and how does Defense-in-Depth support it?</b></summary>
<br>
<b>Answer:</b><br>
<b>The 4 Phases:</b>
<ol>
  <li><b>Protect:</b> Implement baseline safeguards to resist attacks[cite: 3].</li>
  <li><b>Detect:</b> Monitor network activity to identify active intrusions[cite: 3].</li>
  <li><b>Respond:</b> Contain threats and isolate compromised endpoints immediately[cite: 3].</li>
  <li><b>Predict:</b> Utilize threat intelligence to anticipate incoming attack vectors[cite: 3].</li>
</ol>
<b>Defense-in-Depth:</b> Places redundant controls across <b>People</b> (training), <b>Operations</b> (incident response policies), and <b>Technology</b> (firewalls, encryption) so if one layer fails, subsequent layers prevent a total breach[cite: 3].
</details>

---

### Module 02: Administrative Network Security and Governance

<details>
<summary><b>📇 Flashcard 6: What are the 3 phases of the Security Policy Engineering Lifecycle?</b></summary>
<br>
<b>Answer:</b>
<ol>
  <li><b>Design & Development:</b> Defining mandatory rules for acceptable use, password complexity, remote work access, data classification, and incident management[cite: 4].</li>
  <li><b>Enforcement & Oversight:</b> Implementing technical controls that enforce policy rules automatically (e.g., Active Directory group policies)[cite: 4].</li>
  <li><b>Review & Maintenance:</b> Periodically updating policy guidelines to account for emerging technological shifts and newly discovered threats[cite: 4].</li>
</ol>
</details>

<details>
<summary><b>📇 Flashcard 7: What are the three core requirements of effective IT Asset Management (ITAM)?</b></summary>
<br>
<b>Answer:</b>
<ul>
  <li><b>Real-time Asset Inventories:</b> Categorizing devices by IP address, MAC address, operational owner, and physical location[cite: 4].</li>
  <li><b>Security Baseline Configurations:</b> Ensuring every newly deployed system meets minimum security hardening standards before joining the production environment[cite: 4].</li>
  <li><b>Lifecycle Tracking:</b> Managing assets from acquisition through operational maintenance to safe <b>Data Destruction</b> and hardware retirement[cite: 4].</li>
</ul>
</details>

---

### Module 03: Technical Network Security Controls and Protocols

<details>
<summary><b>📇 Flashcard 8: Distinguish between DAC, MAC, RBAC, and IAM access control models.</b></summary>
<br>
<b>Answer:</b>
<ul>
  <li><b>Discretionary Access Control (DAC):</b> The owner of an asset explicitly sets permission levels for other users[cite: 5].</li>
  <li><b>Mandatory Access Control (MAC):</b> Access decisions are determined by a centralized security authority based on formal security classifications and clearances[cite: 5].</li>
  <li><b>Role-Based Access Control (RBAC):</b> Permissions are assigned to specific organizational roles rather than individual user accounts[cite: 5].</li>
  <li><b>Identity and Access Management (IAM):</b> A centralized framework for identity verification, account provisioning, authentication (e.g., MFA), and authorization across distributed and mobile environments[cite: 5].</li>
</ul>
</details>

<details>
<summary><b>📇 Flashcard 9: What is the difference between SHA and HMAC?</b></summary>
<br>
<b>Answer:</b>
<ul>
  <li><b>Secure Hashing Algorithms (SHA):</b> Cryptographic hash functions (like SHA-2 and SHA-3) that generate a fixed-size mathematical signature from variable-length data to verify <b>Data Integrity</b>[cite: 5].</li>
  <li><b>Hash-based Message Authentication Code (HMAC):</b> Combines a cryptographic hash function with a <b>secret shared key</b>, providing both <b>data integrity verification</b> and <b>message authentication</b>[cite: 5].</li>
</ul>
</details>

<details>
<summary><b>📇 Flashcard 10: How do S/MIME and PGP differ in how they secure email?</b></summary>
<br>
<b>Answer:</b><br>
Both provide email authentication and encryption, but[cite: 6]:
<ul>
  <li><b>S/MIME (Secure/Multipurpose Internet Mail Extensions):</b> Uses a centralized Public Key Infrastructure (PKI) with CA-signed X.509 certificates[cite: 6].</li>
  <li><b>PGP (Pretty Good Privacy):</b> Relies on a decentralized "Web of Trust"[cite: 6].</li>
</ul>
</details>

<details>
<summary><b>📇 Flashcard 11: In IPsec, what is the difference between AH vs. ESP, and Transport Mode vs. Tunnel Mode?</b></summary>
<br>
<b>Answer:</b><br>
<b>Protocols (OSI Layer 3):</b>
<ul>
  <li><b>Authentication Header (AH):</b> Provides connectionless integrity and data origin authentication, but <b>does NOT provide encryption/confidentiality</b>[cite: 6].</li>
  <li><b>Encapsulating Security Payload (ESP):</b> Provides packet-level confidentiality (encryption), data origin authentication, and integrity protection[cite: 6].</li>
</ul>
<b>Modes:</b>
<ul>
  <li><b>Transport Mode:</b> Encrypts only the payload of the IP packet while leaving the original IP header intact (used for host-to-host communications)[cite: 6].</li>
  <li><b>Tunnel Mode:</b> Encrypts the entire original IP packet (header and payload) and encapsulates it inside a brand new IP header (essential for Site-to-Site VPN tunnels)[cite: 6].</li>
</ul>
</details>

---

### Module 04: Network Perimeter Security and Defense Architecture

<details>
<summary><b>📇 Flashcard 12: Compare the 5 Firewall Technologies across the OSI Model.</b></summary>
<br>
<b>Answer:</b>
<ul>
  <li><b>Packet Filtering Firewalls (Layers 3 & 4):</b> Inspect packet headers (source/dest IP, port, protocol) without tracking connection state[cite: 7].</li>
  <li><b>Circuit-Level Gateways (Layer 5):</b> Validate the session establishment handshake (e.g., TCP 3-way handshake) before allowing a connection[cite: 7].</li>
  <li><b>Application-Level Firewalls / Proxies (Layer 7):</b> Intercept traffic at Layer 7 and inspect application-level payload data (e.g., blocking malicious HTTP GET requests)[cite: 7].</li>
  <li><b>Stateful Multilayer Inspection Firewalls:</b> Combine header analysis with active connection state tracking tables to ensure incoming packets match an established outgoing TCP session[cite: 7].</li>
  <li><b>Next-Generation Firewalls (NGFW):</b> Integrate stateful inspection with Deep Packet Inspection (DPI), inline IPS, cloud threat intelligence, and user/application-level visibility[cite: 7].</li>
</ul>
</details>

<details>
<summary><b>📇 Flashcard 13: Compare Snort, Suricata, Zeek/Bro, and OSSEC/Wazuh.</b></summary>
<br>
<b>Answer:</b>
<ul>
  <li><b>Snort:</b> Open-source signature-based NIDS engine[cite: 8].</li>
  <li><b>Suricata:</b> Open-source multi-threaded NIDS/IPS engine[cite: 8].</li>
  <li><b>Zeek/Bro:</b> Network analysis framework often combined with ELK logging stacks[cite: 8, 13].</li>
  <li><b>OSSEC / Wazuh:</b> Comprehensive open-source host inspection (HIDS) and telemetry frameworks[cite: 8].</li>
</ul>
</details>

<details>
<summary><b>📇 Flashcard 14: What are the 4 core Switch & Router Hardening measures against Layer 2 attacks?</b></summary>
<br>
<b>Answer:</b>
<ol>
  <li>Disable unused physical switch ports and assign them to an isolated, unused VLAN[cite: 8].</li>
  <li>Enable <b>Port Security</b> to limit the maximum number of allowable MAC addresses learned on a switch port[cite: 8].</li>
  <li>Implement <b>DHCP Snooping</b> to block untrusted DHCP server messages, paired with <b>Dynamic ARP Inspection (DAI)</b> to neutralize ARP poisoning[cite: 8].</li>
  <li>Configure management plane protections by disabling Telnet/HTTP in favor of <b>SSHv2</b> and <b>HTTPS</b>, and enforcing strong <b>AAA authentication</b>[cite: 8].</li>
</ol>
</details>

<details>
<summary><b>📇 Flashcard 15: What are the 3 core components of a Zero Trust Software-Defined Perimeter (SDP), and what is a "dark host"?</b></summary>
<br>
<b>Answer:</b>
<ol>
  <li><b>SDP Controller:</b> The central authority that authenticates devices and users, determines access permissions, and issues trust tokens[cite: 9].</li>
  <li><b>SDP Initiating Host (IH):</b> The client device requesting access to a network resource[cite: 9].</li>
  <li><b>SDP Accepting Host (AH):</b> The protected infrastructure asset that accepts incoming connections only after receiving explicit authorization commands directly from the SDP Controller[cite: 9].</li>
</ol>
<b>Dark Host:</b> Because protected resources refuse unauthenticated traffic, they remain completely hidden from internet scanners until explicit authentication occurs[cite: 9].
</details>

---

## 📝 Part 2: CND Exam Practice Quiz (Multiple Choice, Scenario & True/False)

### Question 1: Network Segmentation
**Which network segmentation technique separates a network into multiple smaller broadcast domains at Layer 2?**[cite: 12]
* A) VLAN[cite: 12]
* B) Subnetting[cite: 12]
* C) NAT[cite: 12]
* D) VPN[cite: 12]

<details>
<summary><b>🔍 Reveal Answer & Explanation</b></summary>
<br>
<b>Correct Answer: A) VLAN</b>[cite: 12]<br>
<b>Explanation:</b> VLANs (Virtual Local Area Networks) logically segment a network into separate broadcast domains at Layer 2, improving security and performance[cite: 12]. Subnetting divides IP address ranges at Layer 3 but does not inherently create separate Layer 2 broadcast domains[cite: 12].
</details>

---

### Question 2: VPN & Network Protocols
**Which protocol suite operates at OSI Layer 3 to provide encryption, integrity, and authentication, and is widely used in Tunnel Mode for site-to-site VPNs?**[cite: 6, 12]
* A) PPTP[cite: 12]
* B) L2TP[cite: 12]
* C) IPsec[cite: 6, 12]
* D) S/MIME[cite: 6]

<details>
<summary><b>🔍 Reveal Answer & Explanation</b></summary>
<br>
<b>Correct Answer: C) IPsec</b>[cite: 12]<br>
<b>Explanation:</b> IPsec (Internet Protocol Security) operates at the Network Layer (Layer 3) and provides confidentiality, integrity, and authentication (via ESP)[cite: 6, 12]. In Tunnel Mode, it encrypts the entire original IP packet (header and payload) and encapsulates it inside a new IP header for Site-to-Site VPNs[cite: 6]. PPTP is outdated and insecure, while L2TP relies on IPsec for encryption[cite: 12].
</details>

---

### Question 3: Scenario — Layer 2 Infrastructure Defense
**Scenario:** Users on a corporate subnet report intermittent connectivity issues and warning prompts about invalid SSL certificates. Upon investigating the local switch, a network defender discovers that host traffic is being routed through an unauthorized laptop on the floor instead of the legitimate default gateway. 

**Which combination of switch hardening features should the defender enable to neutralize this specific attack vector and prevent a rogue DHCP server from being deployed?**[cite: 2, 8]
* A) Packet Filtering and Circuit-Level Gateways[cite: 7]
* B) DHCP Snooping and Dynamic ARP Inspection (DAI)[cite: 8]
* C) Role-Based Access Control (RBAC) and HMAC[cite: 5]
* D) IPsec Transport Mode and TLS[cite: 6]

<details>
<summary><b>🔍 Reveal Answer & Explanation</b></summary>
<br>
<b>Correct Answer: B) DHCP Snooping and Dynamic ARP Inspection (DAI)</b>[cite: 8]<br>
<b>Explanation:</b> The attacker is executing an <b>ARP Poisoning</b> Man-in-the-Middle (MitM) attack (associating their MAC address with the legitimate default gateway's IP) or a <b>DHCP Spoofing</b> attack[cite: 2]. Enabling <b>DHCP Snooping</b> blocks untrusted DHCP server messages, and pairing it with <b>Dynamic ARP Inspection (DAI)</b> neutralizes ARP poisoning on the switch[cite: 8].
</details>

---

### Question 4: Scenario — Switch Binding Table Exhaustion
**Scenario:** An attacker connects to an active ethernet jack in a conference room and floods the network switch with thousands of frames containing forged source MAC addresses. Shortly after, the switch begins broadcasting unicast traffic out of all physical ports, allowing the attacker to sniff traffic across the subnet.

**What attack has occurred, and which control directly prevents it?**[cite: 2, 8]
* A) Birthday Attack; mitigated by SHA-3[cite: 2, 5]
* B) Switch Port Stealing / MAC Duplicating; mitigated by Port Security[cite: 2, 8]
* C) Rainbow Table Attack; mitigated by HMAC[cite: 2, 5]
* D) DNS Footprinting; mitigated by a DMZ[cite: 2, 5]

<details>
<summary><b>🔍 Reveal Answer & Explanation</b></summary>
<br>
<b>Correct Answer: B) Switch Port Stealing / MAC Duplicating; mitigated by Port Security</b>[cite: 2, 8]<br>
<b>Explanation:</b> Flooding switch binding tables forces a switch into hub-like behavior where it exposes unicast traffic across all physical ports[cite: 2]. Enabling <b>Port Security</b> limits the maximum number of allowable MAC addresses learned on a single physical switch port[cite: 8].
</details>

---

### Question 5: Cryptographic Controls
**A network architect needs to ensure that configuration messages sent between two internal servers have not been altered in transit (Data Integrity) AND verify that the messages genuinely originated from the authorized sender using a shared secret key. Which cryptographic mechanism should be used?**[cite: 5]
* A) SHA-2 alone[cite: 5]
* B) HMAC (Hash-based Message Authentication Code)[cite: 5]
* C) IPsec Authentication Header (AH) in Tunnel Mode[cite: 6]
* D) Discretionary Access Control (DAC)[cite: 5]

<details>
<summary><b>🔍 Reveal Answer & Explanation</b></summary>
<br>
<b>Correct Answer: B) HMAC (Hash-based Message Authentication Code)</b>[cite: 5]<br>
<b>Explanation:</b> While SHA-2 verifies data integrity via a fixed-size mathematical signature, <b>HMAC</b> combines a cryptographic hash function with a secret shared key to provide both <b>data integrity verification</b> and <b>message authentication</b>[cite: 5].
</details>

---

### Question 6: IDS/IPS Operations & Tuning
**An administrator deploys Suricata inline to actively drop malicious packets automatically. However, legitimate employee web traffic is suddenly being blocked because an overly broad rule is flagging benign HTTP requests as attacks. How is this tuning issue classified?**[cite: 7, 8]
* A) False Negative in a HIDS deployment[cite: 8]
* B) False Positive in an IPS deployment[cite: 7, 8]
* C) False Negative in a NIDS deployment[cite: 8]
* D) True Positive in a Packet Filtering Firewall[cite: 7]

<details>
<summary><b>🔍 Reveal Answer & Explanation</b></summary>
<br>
<b>Correct Answer: B) False Positive in an IPS deployment</b>[cite: 7, 8]<br>
<b>Explanation:</b> Because the system sits directly inline to actively drop packets automatically, it is operating as an <b>Intrusion Prevention System (IPS)</b>[cite: 7]. When benign traffic is incorrectly flagged as malicious, it is a <b>False Positive</b> (whereas missing actual malicious traffic is a <b>False Negative</b>)[cite: 8].
</details>

---

### Question 7: Access Control Models
**In a military or highly classified government network, users are not permitted to change permissions on files they create. Instead, a centralized authority grants access strictly based on formal security classifications and user clearance levels. Which access control model is in use?**[cite: 5]
* A) Discretionary Access Control (DAC)[cite: 5]
* B) Role-Based Access Control (RBAC)[cite: 5]
* C) Mandatory Access Control (MAC)[cite: 5]
* D) Software-Defined Perimeter (SDP)[cite: 8]

<details>
<summary><b>🔍 Reveal Answer & Explanation</b></summary>
<br>
<b>Correct Answer: C) Mandatory Access Control (MAC)</b>[cite: 5]<br>
<b>Explanation:</b> In <b>MAC</b>, access decisions are determined by a centralized security authority based on formal security classifications and clearances[cite: 5]. In <b>DAC</b>, the asset owner sets permissions, and in <b>RBAC</b>, permissions are tied to organizational job roles[cite: 5].
</details>

---

### Question 8: True / False — IPsec Protocols
**True or False: The IPsec Authentication Header (AH) protocol encrypts packet payloads to ensure confidentiality across untrusted networks.**[cite: 6]

<details>
<summary><b>🔍 Reveal Answer & Explanation</b></summary>
<br>
<b>Correct Answer: False</b>[cite: 6]<br>
<b>Explanation:</b> Authentication Header (AH) provides connectionless integrity and data origin authentication for IP packets, but <b>does NOT provide encryption/confidentiality</b>[cite: 6]. To achieve packet-level encryption (confidentiality), you must use <b>Encapsulating Security Payload (ESP)</b>[cite: 6].
</details>

---

### Question 9: Firewall Evolution
**Which firewall technology operates strictly at Layer 5 of the OSI model to validate session establishment handshakes (such as the TCP 3-way handshake) without inspecting Layer 7 application payloads?**[cite: 7]
* A) Packet Filtering Firewall[cite: 7]
* B) Circuit-Level Gateway[cite: 7]
* C) Application Proxy[cite: 7]
* D) Next-Generation Firewall (NGFW)[cite: 7]

<details>
<summary><b>🔍 Reveal Answer & Explanation</b></summary>
<br>
<b>Correct Answer: B) Circuit-Level Gateway</b>[cite: 7]<br>
<b>Explanation:</b> Circuit-Level Gateways validate session establishment handshakes at Layer 5 before allowing a connection[cite: 7]. Packet filtering operates at Layers 3 and 4, Application Proxies inspect payloads at Layer 7, and NGFWs combine stateful inspection with Deep Packet Inspection (DPI) and inline IPS[cite: 7].
</details>

---

### Question 10: Zero Trust Architecture
**In a Software-Defined Perimeter (SDP) architecture, which component represents the protected server/infrastructure asset that remains invisible ("dark") until explicitly authorized to accept a connection?**[cite: 9]
* A) SDP Controller[cite: 9]
* B) SDP Initiating Host (IH)[cite: 9]
* C) SDP Accepting Host (AH)[cite: 9]
* D) Demilitarized Zone (DMZ)[cite: 5]

<details>
<summary><b>🔍 Reveal Answer & Explanation</b></summary>
<br>
<b>Correct Answer: C) SDP Accepting Host (AH)</b>[cite: 9]<br>
<b>Explanation:</b> The <b>SDP Accepting Host (AH)</b> is the protected infrastructure asset that accepts incoming connections only after receiving explicit authorization commands directly from the <b>SDP Controller</b>[cite: 9]. The client device requesting access is the <b>SDP Initiating Host (IH)</b>[cite: 9].
</details>

---

## 🎤 Part 3: Blue-Team Interview Prep Questions

Practicing CND concepts also prepares you for technical interviews in network defense roles[cite: 12]. Try answering these out loud before checking the key points:

<details>
<summary><b>💬 Interview Q1: Explain the difference between a stateful and stateless firewall.</b></summary>
<br>
<b>Key Talking Points:</b>
<ul>
  <li>A <b>stateless (Packet Filtering) firewall</b> inspects individual packet headers (source/destination IP, port, protocol) at Layers 3 and 4 in isolation without tracking connection state[cite: 7, 12].</li>
  <li>A <b>stateful (Stateful Multilayer Inspection) firewall</b> combines header analysis with active connection state tracking tables, ensuring incoming packets match an established outgoing TCP session[cite: 7, 12].</li>
</ul>
</details>

<details>
<summary><b>💬 Interview Q2: What is the role of a DMZ in network security?</b></summary>
<br>
<b>Key Talking Points:</b>
<ul>
  <li>A <b>Demilitarized Zone (DMZ)</b> is a physical or logical subnet that separates an enterprise's internal private network from untrusted public networks like the Internet[cite: 5, 12].</li>
  <li>Public-facing servers (Web, DNS, Email) reside in the DMZ between perimeter firewalls so that if a public server is compromised, direct lateral movement to sensitive internal workstations, databases, and domain controllers remains blocked[cite: 5, 6].</li>
</ul>
</details>

<details>
<summary><b>💬 Interview Q3: How would you detect and mitigate a Man-in-the-Middle (MitM) attack on your local network?</b></summary>
<br>
<b>Key Talking Points:</b>
<ul>
  <li><b>Detection:</b> Monitor network traffic with NIDS solutions (like Snort, Suricata, or Zeek) at switch SPAN/TAP ports to spot duplicate IP-to-MAC mappings, anomalous ARP broadcasts, or rogue DHCP offers[cite: 2, 8, 12].</li>
  <li><b>Mitigation:</b> Enable switch-level protections including <b>DHCP Snooping</b>, <b>Dynamic ARP Inspection (DAI)</b>, and <b>Port Security</b>, and enforce strong cryptographic protocols in transit like <b>TLS/HTTPS</b> and <b>IPsec (ESP)</b>[cite: 6, 8].</li>
</ul>
</details>

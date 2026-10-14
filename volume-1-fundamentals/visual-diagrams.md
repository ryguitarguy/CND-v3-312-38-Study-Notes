# 📊 CND v3 Volume 1: Visual Architecture & Taxonomy Diagrams

These visual diagrams are rendered natively using **Mermaid.js** and cover the core architectures, taxonomies, and protocol flows in Volume 1 (Modules 1–4)[cite: 1, 3, 6, 9].

---

## 1. Module 01: Threat & Defense Taxonomy (Mind Map)
This branching diagram visualizes the expanded Information Assurance (IA) principles, threat actor classes, network-level attack vectors, and the Continual/Adaptive Security framework[cite: 1, 2, 3].

```mermaid
mindmap
  root((CND Volume 1<br/>Threat & Defense<br/>Taxonomy))
    Information Assurance (IA)
      Confidentiality
      Integrity
      Availability
      Authentication
      Non-repudiation
    Threat Actors
      Script Kiddies
      Hacktivists
      Insider Threats
      Organized Cybercriminals & Spies
      State-Sponsored Hackers
    Network Attack Vectors
      Reconnaissance
        DNS Footprinting
        Network Sniffing
        Port Scanning
      Man-in-the-Middle (MitM)
      Password Exploitation
        Dictionary & Brute Force
        Hybrid Attacks
        Rainbow Tables
        Birthday Attacks
      Layer 2 Infrastructure
        ARP Poisoning
        DHCP Starvation & Spoofing
        Switch Port Stealing / MAC Duplicating
      DoS / DDoS
    Adaptive Defense Strategy
      1. Protect
      2. Detect
      3. Respond
      4. Predict
      Defense-in-Depth
        People
        Operations
        Technology
```

---

## 2. Module 01: Continual/Adaptive Security & Defense-in-Depth
Defending against modern vectors requires cycling continuously through four operational phases while placing redundant controls across People, Operations, and Technology[cite: 3].

```mermaid
flowchart LR
    subgraph Adaptive_Cycle ["🔄 Continual / Adaptive Security Strategy"]
        direction TB
        P["1. Protect<br/>(Baseline Safeguards)"] --> D["2. Detect<br/>(Monitor Activity)"]
        D --> R["3. Respond<br/>(Contain & Isolate)"]
        R --> PR["4. Predict<br/>(Threat Intelligence)"]
        PR --> P
    end

    subgraph DiD ["🛡️ Defense-in-Depth (Multi-Layered Controls)"]
        direction TB
        L1["👥 People<br/>(Security Awareness Training)"]
        L2["📋 Operations<br/>(Policies & Incident Response)"]
        L3["💻 Technology<br/>(Firewalls, IDS/IPS, Encryption)"]
        L1 --> L2 --> L3
    end

    Adaptive_Cycle <==>|Operationalizes| DiD
```

---

## 3. Module 02: Security Policy Lifecycle & IT Asset Management (ITAM)
Technical safeguards rely on administrative governance, structured policy engineering, and full-lifecycle IT asset tracking[cite: 3, 4].

```mermaid
flowchart TD
    subgraph Policy ["📜 Security Policy Engineering Lifecycle"]
        P1["1. Design & Development<br/>(Acceptable Use, Passwords, Remote Work, Data Class)"] --> P2["2. Enforcement & Oversight<br/>(Automated Controls, e.g., AD Group Policies)"]
        P2 --> P3["3. Review & Maintenance<br/>(Update for Emerging Tech & New Threats)"]
        P3 -.->|Continuous Improvement| P1
    end

    subgraph ITAM ["🖥️ IT Asset Management (ITAM) Lifecycle"]
        A1["1. Acquisition & Real-Time Inventory<br/>(Track IP, MAC, Owner, Physical Location)"] --> A2["2. Security Baseline Configuration<br/>(Minimum Hardening Before Production)"]
        A2 --> A3["3. Operational Maintenance<br/>(Patching & Monitoring)"]
        A3 --> A4["4. Safe Data Destruction<br/>& Hardware Retirement"]
    end
```

---

## 4. Module 03: Demilitarized Zone (DMZ) Network Segmentation
A DMZ separates the internal private network from untrusted public networks so that if a public-facing server is compromised, direct lateral movement to sensitive internal assets remains blocked[cite: 5, 6, 12].

```mermaid
flowchart TD
    Internet(["🌐 UNTRUSTED INTERNET"])
    FW1{{"🔥 External Perimeter Firewall"}}
    
    subgraph DMZ ["⚠️ Demilitarized Zone (DMZ) Subnet"]
        Web["🌍 Web Server (HTTPS/TLS)"]
        DNS["🧭 DNS Server (DNSSEC)"]
        Mail["✉️ Email Server (S/MIME, PGP)"]
    end

    FW2{{"🔥 Internal Boundary Firewall"}}

    subgraph Internal ["🔒 SECURE INTERNAL NETWORK"]
        WS["💻 Employee Workstations"]
        DB[("🗄️ Internal Databases")]
        DC["🔑 Domain Controllers (IAM / AD)"]
    end

    Internet ===>|Public Traffic| FW1
    FW1 ===>|Filtered Public Requests| DMZ
    DMZ -.->| ❌ Direct Internal Access Blocked| FW2
    FW1 ===>|Strictly Inspected Stateful Traffic| FW2
    FW2 ===>|Authorized Internal Traffic| Internal
```

---

## 5. Module 03: Technical Security Controls & IPsec Comparison
A comparative breakdown of Access Control Models, Cryptographic Hashing Primitives, and IPsec Protocols/Modes[cite: 5, 6, 12].

```mermaid
flowchart TB
    subgraph Access ["🔑 Access Control Models"]
        DAC["<b>DAC (Discretionary)</b><br/>Asset owner sets permissions"]
        MAC["<b>MAC (Mandatory)</b><br/>Central authority + clearances"]
        RBAC["<b>RBAC (Role-Based)</b><br/>Permissions tied to job roles"]
        IAM["<b>IAM Framework</b><br/>Central provisioning + MFA"]
    end

    subgraph Crypto ["🔐 Cryptographic Integrity & Auth"]
        SHA["<b>SHA (SHA-2 / SHA-3)</b><br/>Fixed-size hash signature<br/>✅ Data Integrity ONLY"]
        HMAC["<b>HMAC</b><br/>Hash function + Secret Shared Key<br/>✅ Integrity + ✅ Authentication"]
    end

    subgraph IPsec ["🛡️ IPsec Suite (OSI Layer 3)"]
        direction LR
        subgraph Protocols ["IPsec Protocols"]
            AH["<b>Authentication Header (AH)</b><br/>✅ Integrity & Origin Auth<br/>❌ NO Encryption"]
            ESP["<b>Encapsulating Security Payload (ESP)</b><br/>✅ Confidentiality (Encryption)<br/>✅ Integrity & Origin Auth"]
        end
        subgraph Modes ["IPsec Operational Modes"]
            Trans["<b>Transport Mode</b><br/>Encrypts IP Payload ONLY<br/>Original IP Header Intact<br/>(Host-to-Host)"]
            Tunn["<b>Tunnel Mode</b><br/>Encrypts Entire Original Packet<br/>Adds New IP Header<br/>(Site-to-Site VPN)"]
        end
    end
```

---

## 6. Module 04: Firewall Evolution Across the OSI Model
Firewalls have evolved from basic stateless header inspection to multi-layered Deep Packet Inspection (DPI) and inline intrusion prevention[cite: 7, 12].

```mermaid
flowchart BT
    L34["<b>Layers 3 & 4: Packet Filtering Firewall</b><br/>Inspects Source/Dest IP, Port, Protocol (Stateless)"]
    L5["<b>Layer 5: Circuit-Level Gateway</b><br/>Validates Session Handshakes (e.g., TCP 3-Way Handshake)"]
    State["<b>Layers 3–5: Stateful Multilayer Inspection</b><br/>Tracks Active Connection State Tables"]
    L7["<b>Layer 7: Application-Level Firewall / Proxy</b><br/>Inspects Application Payload Data (e.g., HTTP GET Requests)"]
    NGFW["<b>Multi-Layer: Next-Generation Firewall (NGFW)</b><br/>Stateful Inspection + Deep Packet Inspection (DPI) + Inline IPS + Threat Intel"]

    L34 --> L5 --> State --> L7 --> NGFW
```

---

## 7. Module 04: Zero Trust Software-Defined Perimeter (SDP) Workflow
Operating under *"Never Trust, Always Verify,"* SDP hides protected infrastructure as "dark hosts" until the central SDP Controller explicitly authenticates the user/device and authorizes a dynamic one-to-one encrypted connection[cite: 8, 9, 12, 13].

```mermaid
sequenceDiagram
    autonumber
    actor IH as 💻 SDP Initiating Host (IH)<br/>(Client Device)
    participant Ctrl as 🧠 SDP Controller<br/>(Central Authority)
    participant AH as 🛡️ SDP Accepting Host (AH)<br/>(Protected "Dark Host" Server)

    Note over IH,AH: Protected servers remain completely hidden ("Dark Hosts") from unauthenticated scanners
    IH->>Ctrl: 1. Request Access (Present Identity & Device Posture)
    Ctrl->>Ctrl: 2. Verify Identity, Device & Access Policy
    Ctrl->>AH: 3. Send Explicit Authorization Command (Allow IH)
    Ctrl->>IH: 4. Issue Trust Token & Connection Details
    IH->>AH: 5. Establish Dynamic 1-to-1 Encrypted Tunnel
    Note over IH,AH: Authorized session active strictly for the permitted application
```

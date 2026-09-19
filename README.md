# Home-Lab-SOC
A Proxmox-based cybersecurity home lab for developing practical SOC Analyst, Networking, Linux, Virtualization, Docker, Coding and Software Development/Engineering, and self-hosting skills.

The primary focus of this environment is developing hands-on SOC Analyst skills through controlled attack simulations, security monitoring, alert investigation, incident documentation, and defensive security experimentation.

# 🎯 Project Goals
The primary goals of this home lab are to:
Develop practical SOC Analyst skills
Learn and practice SIEM operations
Perform controlled security testing
Investigate security events and alerts
Practice incident response
Develop Linux and Windows administration skills
Learn networking and network security
Gain experience with virtualization
Learn Docker and self-hosted services
Build a portfolio demonstrating hands-on cybersecurity experience

# 🏗️ Lab Overview
The lab is built on a Proxmox virtualization server and currently contains seven virtual machines.
| VM | ID | Primary Purpose |
|---|---|---|
| TrueNAS | 100 | Storage and file management |
| ZimaOS | 101 | Self-hosting experimentation |
| Kali Linux | 102 | Security testing and attack simulation |
| Ubuntu Server | 103 | Linux, Docker, and SOC services |
| Bodhi Linux | 104 | Pi Agent coding experimentation |
| Windows 11 | 105 | Monitored endpoint and security testing target
| EVE-NG | 106 | Networking laboratory |


# 🛡️ SOC Environment
The SOC environment is the primary focus of this project.
The current SOC stack consists of:
- Kali Linux — attack simulation and security testing
- Windows 11 — monitored endpoint
- Ubuntu Server — Docker host
- Wazuh — SIEM and security monitoring
- Zammad — incident/ticket management
- Code-Server — development environment

The current workflow is designed around:
Attack Simulation
       │
       ▼
   Target Host
       │
       ▼
Security Telemetry
       │
       ▼
     Wazuh
       │
       ▼
 Alert / Event
       │
       ▼
 Investigation
       │
       ▼
Incident Documentation
       │
       ▼
    Zammad

# 🔎 Current SOC Capabilities
The lab currently supports:
- Windows endpoint monitoring
- Kali Linux monitoring
- Windows Security event collection
- Successful and failed login monitoring
- Wazuh SIEM experimentation
- Controlled network reconnaissance
- Security event investigation
- Docker-based security services

Both the Windows 11 and Kali Linux systems are currently connected to Wazuh as agents.

# 🧪 Current Security Exercise
The first documented security exercise involves using Kali Linux to perform controlled Nmap reconnaissance against the Windows 11 endpoint.
Objective:
- Determine whether the current Wazuh deployment can detect and provide useful telemetry for network reconnaissance.

The investigation will examine:
- Windows security telemetry
- Network-related events
- Wazuh alerts
- Source and destination information
- Detection capabilities
- Detection gaps

See: [001 Nmap Reconnaissance](soc/attack-scenarios/001-nmap-reconnaissance/README.md)

# 🌐 Network Architecture
The current lab uses a simple single-network design.
                   HOME NETWORK
                         │
                         ▼
                 ┌──────────────┐
                 │ Home Router  │
                 │ DHCP / LAN   │
                 └──────┬───────┘
                        │
                        ▼
                 ┌──────────────┐
                 │   Proxmox    │
                 │    Server    │
                 └──────┬───────┘
                        │
                  Virtual Network
                        │
       ┌────────────────┼────────────────┐
       │       │        │       │        │
       ▼       ▼        ▼       ▼        ▼
     Kali   Windows   Ubuntu  TrueNAS   ZimaOS
       │       │        │
       │       │        ├── Wazuh
       │       │        ├── Zammad
       │       │        └── Code-Server
       │       │
       └───────┴─────────────────────────┐
                                         │
                               Same Network Environment
                                         │
                              ┌──────────┴──────────┐
                              ▼                     ▼
                         Bodhi Linux             EVE-NG
The current environment does not use VLANs or dedicated network segments.
Network segmentation may be explored in the future as the lab develops.

# 🖥️ Infrastructure
- Virtualization
  - Proxmox
- Operating Systems
  - TrueNAS
  - ZimaOS
  - Kali Linux
  - Ubuntu Server
  - Bodhi Linux
  - Windows 11
  - EVE-NG
- Security
  - Wazuh
  - Kali Linux
  - Windows Security telemetry
- Self-Hosting
  - Docker
  - Wazuh
  - Zammad
  - Code-Server
  - TrueNAS
  - ZimaOS
- Networking
  - EVE-NG
  - Proxmox virtual networking
  - Home LAN

# 📚 Areas of Learning
This environment is being used to develop skills in:
- SOC Operations
- SIEM
- Security Monitoring
- Incident Response
- Network Security
- Linux Administration
- Windows Administration
- Docker
- Virtualization
- Networking
- Self-Hosting
- Coding & Software Development/Engineering
- Cybersecurity

# 🚧 Planned Development
The lab will evolve over time.

SOC
- [ ] Deploy Wazuh
- [ ] Connect Windows 11 agent
- [ ] Connect Kali Linux agent
- [ ] Collect Windows Security events
- [ ] Monitor successful/failed logins
- [ ] Create first Nmap reconnaissance exercise
- [ ] Complete Nmap detection investigation
- [ ] Create custom detection rules
- [ ] Create additional attack scenarios
- [ ] Document security investigations
- [ ] Develop incident response workflow
- [ ] Integrate Zammad into incident management
- [ ] Map detections to MITRE ATT&CK techniques

Infrastructure
- [ ] Deploy Proxmox environment
- [ ] Deploy seven virtual machines
- [ ] Deploy Ubuntu Docker host
- [ ] Deploy Docker-based services
- [ ] Improve documentation
- [ ] Develop backup/recovery procedures
- [ ] Explore automation

Networking
- [ ] Establish basic lab connectivity
- [ ] Deploy EVE-NG
- [ ] Build networking scenarios
- [ ] Practice routing
- [ ] Practice switching
- [ ] Explore network security
- [ ] Explore network segmentation

Self-Hosting
- [ ] Deploy TrueNAS
- [ ] Deploy ZimaOS
- [ ] Deploy Docker
- [ ] Deploy Zammad
- [ ] Deploy Code-Server
- [ ] Explore additional self-hosted services

# 📈 Project Philosophy
The lab is intentionally being developed incrementally.
Rather than attempting to build a fully segmented enterprise environment immediately, the focus is on understanding each technology and developing practical skills through hands-on experimentation.
The long-term goal is to evolve the environment from a basic home lab into a small, documented SOC training environment.

# ⚠️ Security Disclaimer
This environment is intended for authorized testing and education within my own home lab.
Security testing should only be performed against systems that I own or have explicit permission to test.
Sensitive information such as passwords, API keys, private keys, credentials, and other secrets should never be committed to this repository.

# 📌 Project Status
Current Phase: SOC Development / Detection Engineering

Primary Focus: SOC Analyst skills

Environment: Proxmox-based home lab

Network: Single home LAN

Primary SIEM: Wazuh

See [My SOC Journal](Small-Home-Lab-SOC/SOC-Journal.md) for updates which is done periodically.

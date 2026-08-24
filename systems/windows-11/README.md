Windows 11

Purpose
- Windows 11 serves as the monitored endpoint and security testing target within the SOC environment.

Resources
- VM ID: 105
- vCPU: 4
- RAM: 12 GB
- Storage: 64 GB

Monitoring
- The Windows 11 VM is connected to Wazuh as an agent.
- Current observed telemetry includes:
  - Windows Security events
  - Successful login events
  - Failed login events

Security Testing
- The system is used as the target for controlled security exercises originating from Kali Linux.

Current Exercise
- Nmap reconnaissance is being used to investigate whether network scanning activity can be detected through the current Wazuh configuration.

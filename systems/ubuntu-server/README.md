Ubuntu Server

Purpose
- Ubuntu Server is the primary Docker host for the SOC and self-hosting services.

Resources
- VM ID: 103
- vCPU: 4
- RAM: 6.88 GB
- Storage: 80 GB

Docker Services
- Wazuh
- Zammad
- Code-Server

Role in SOC
- Ubuntu Server provides the infrastructure hosting the primary SOC applications.
- Wazuh runs using Docker Compose.

Future Work
- Document Docker architecture
- Document persistent storage
- Document container networking
- Improve backup/recovery procedures
- Explore additional services

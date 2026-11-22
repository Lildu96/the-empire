# Host Inventory

An inventory of the physical machines that make up **The Empire**, including hardware specifications, operating systems and their roles.

## Dexus

**Role:** Primary infrastructure and application server

### System Information

| Property | Details |
|---|---|
| Hostname | `dexus` |
| Manufacturer | Dell |
| Model | Precision 5820 Tower X-Series |
| Operating System | Debian GNU/Linux 13 (Trixie) |
| Architecture | x86-64 |

### Hardware

| Component | Specification |
|---|---|
| Processor | Intel Core i9-9900X @ 3.50 GHz |
| CPU Cores | 10 |
| CPU Threads | 20 |
| Memory | Approximately 64 GB installed (62 GiB usable) |
| Swap | 48 GiB |
| SSD | 1 TB NVMe — CT1000P3PSSD8 |
| HDD | 2 TB SATA — ST2000DM008-2FR102 |

### Responsibilities

Dexus is the primary server responsible for hosting and managing the Empire's infrastructure.

Its services include:

- Docker and containerised applications
- BIND9 internal DNS
- Caddy reverse proxy
- Authentik identity and access management
- Tailscale connectivity
- Prometheus and Grafana monitoring
- Self-hosted applications including Vikunja, Immich and BuJet

### Network Configuration

Network addresses and sensitive operational configuration are maintained separately from this public documentation.

### Notes

Hardware and operating system specifications were collected directly from the host. Application and network configurations will be verified during the service and network audits.


## Nasberrypi

**Role:** Network-attached storage (NAS)

### System Information

| Property | Details |
|---|---|
| Hostname | `nasberrypi` |
| Manufacturer | Raspberry Pi Foundation |
| Model | Raspberry Pi 3 Model B Plus Rev 1.3 |
| Operating System | Debian GNU/Linux 13 (Trixie) |
| Architecture | ARM64 (aarch64) |

### Hardware

| Component | Specification |
|---|---|
| Processor | Quad-core ARM Cortex-A53 |
| CPU Cores | 4 |
| Memory | 1 GB (905 MiB usable) |
| Swap | 904 MiB |
| Primary Storage | 4 TB HDD — Seagate |
| System Storage | 16 GB microSD card (14.8 GiB reported) |

### Responsibilities

Nasberrypi provides shared storage for the Empire's infrastructure and applications.

Its responsibilities include:

- Network-attached storage
- NFS file sharing
- Persistent storage for applications hosted on dexus
- Shared photo storage for Immich

### Notes

- Storage and system hardware details were verified directly on the host.
- NFS exports, mount points and network dependencies will be documented during the storage and network audits.
- Sensitive operational configuration is maintained separately from this public repository.
# 🏰 The Empire

*My personal homelab, infrastructure playground, and ever-evolving collection of self-hosted services.*

## Overview

The Empire is my personal infrastructure project, built to explore Linux, networking, virtualisation, containerisation, security, and self-hosting.

What started as a home server has grown into a collection of interconnected systems, services, and applications.

This repository serves as the central source of truth for the Empire's infrastructure, including system inventories, network configurations, architecture decisions, migration plans, and troubleshooting documentation.

## 🖥️ Infrastructure

| Host | Operating System | Purpose |
|---|---|---|
| **dexus** | Ubuntu Server | Primary application and infrastructure server |
| **nasberrypi** | Raspberry Pi | Network-attached storage |
| **relic** | Fedora Linux | Portable administration and development laptop |
| **altar** | Fedora KDE | Desktop workstation |

### Core technologies

- **Docker & Docker Compose** — Containerised applications
- **Caddy** — Reverse proxy and service routing
- **BIND9** — Internal DNS and split-horizon resolution
- **Tailscale** — Private networking and remote access
- **Authentik** — Identity and access management
- **Prometheus & Grafana** — Monitoring and observability
- **Vikunja** — Project and task management

The Empire also hosts various personal applications, development projects, and experimental services.

## 📚 Documentation

Documentation is organised into the following categories:

| Directory | Contents |
|---|---|
| `inventory/` | Hosts, hardware, applications and services |
| `network/` | DNS, routing, firewalls and network architecture |
| `services/` | Individual application and service documentation |
| `migrations/` | Infrastructure migration plans and implementation notes |
| `runbooks/` | Troubleshooting, maintenance and recovery procedures |

## 🚀 Current Project: The Great Sanctum Shimmy

**Status:** Planning

The Great Sanctum Shimmy is a planned migration of the Empire's infrastructure to a Tailscale-only access model.

### Objectives

- Transition inter-device communication to Tailscale.
- Preserve existing `.dexus` service hostnames.
- Maintain reliable access to self-hosted applications.
- Secure services against unintended LAN access.
- Preserve essential local and container networking.
- Ensure backups, monitoring and recovery procedures are in place.
- Document the final architecture.

The migration is being planned and tracked through Vikunja.

Existing infrastructure will remain operational during preparation, with changes introduced through a controlled migration process.

## 🔧 Documentation Principles

- Document the current configuration before modifying it.
- Explain why architectural decisions were made.
- Test configuration changes before deploying them.
- Maintain backups and rollback procedures.
- Update documentation whenever infrastructure changes.
- Keep documentation understandable and reproducible.

## 🔒 Security

This is a private infrastructure repository.

Sensitive information, including passwords, private keys, authentication tokens, and environment secrets, must never be committed.

Configuration examples should use placeholders where appropriate.

---

*The Empire is never truly finished. There's always something new to build, break, fix, or learn.* 💜

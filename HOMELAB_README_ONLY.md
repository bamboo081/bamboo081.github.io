# Bamboo Homelab

This repository documents my homelab setup, what I have built so far, the services I have tested, and the problems I have worked through along the way.

## Current hardware

- Homelab FiOS router
- Lenovo Legion laptop
- Desktop running Ubuntu as the main homelab machine

## What I have done so far

### Network setup

- reused an older Verizon FiOS router for the homelab
- separated the lab from the main home network into its own segment
- used the homelab router as the boundary for lab testing and services

### System setup

- moved toward Ubuntu as the main operating system for the homelab desktop
- cleaned up earlier boot complexity from older multi-boot experiments
- recovered from boot problems by using a stable working kernel when a newer one failed

### Remote access

- installed and used Tailscale
- tested local and remote connectivity between the laptop and desktop
- evaluated remote desktop quality and lag

### Containers and service hosting

- installed Docker and worked with Docker Compose
- tested Portainer for container management
- started building out Pi-hole for DNS filtering and ad blocking

### DNS and networking work

- investigated why network access could work while domain names still failed to resolve
- diagnosed DNS service conflicts
- worked through resolver and upstream DNS decisions

### Performance and infrastructure testing

- checked Wi-Fi consistency and network bottlenecks
- looked into virtualization / KVM readiness
- explored ways to improve remote desktop speed and quality

## Services tested or planned

### Already tested or partially set up

- Tailscale
- Docker
- Docker Compose
- Portainer
- Pi-hole

### Planned additions

- Uptime Kuma
- Prometheus
- Grafana
- Nextcloud
- Home Assistant
- Caddy or Nginx Proxy Manager

## Main lessons so far

- separating the homelab from the main network makes testing much easier
- DNS problems can look like total internet failure even when the network is still up
- remote access quality depends on more than bandwidth alone
- self-hosting is as much about debugging and observability as it is about launching services

## Current status

### Working

- separate homelab network concept
- Ubuntu homelab machine
- Tailscale connectivity
- basic container stack direction

### In progress

- Pi-hole / DNS filtering
- service reliability
- better remote desktop quality
- monitoring and dashboards

### Still being debugged

- DNS resolution edge cases
- container networking conflicts
- virtualization readiness
- Wi-Fi consistency

## Note

This public version leaves out sensitive information such as private IP addresses, local hostnames, and other network-specific identifiers.

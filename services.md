---
layout: default
title: Services
---

<div class="top-nav">
  <a href="{{ '/' | relative_url }}">Home</a>
  <a href="{{ '/timeline' | relative_url }}">Timeline</a>
  <a href="{{ '/services' | relative_url }}">Services</a>
  <a href="{{ '/troubleshooting' | relative_url }}">Troubleshooting</a>
</div>

# Services and experiments

## Already tested or partially set up

### Tailscale

Used for secure remote connectivity between devices in the homelab and for reaching systems when away from home.

### Docker / Docker Compose

The main deployment direction for homelab services. Containers are the easiest way to keep experiments organized and reproducible.

### Portainer

Used as a management layer for containers. Helpful for quickly seeing what is running, what failed, and what ports or volumes are in use.

### Pi-hole

One of the main network-level services I worked on. The goal is DNS-based filtering and better control over what devices resolve on the network.

## Services I have planned for the lab

### Uptime Kuma

To monitor whether machines and services are actually online.

### Prometheus + Grafana

For metrics, dashboards, and longer-term visibility into system health and performance.

### Nextcloud

For personal cloud storage, syncing, and self-hosted file access.

### Home Assistant

For local smart-home control and automation later on.

### Reverse proxy layer

Either:

- Caddy
- Nginx Proxy Manager

The purpose is to make self-hosted services easier to expose internally, organize, and secure.

## What this stack is turning into

The long-term direction is a homelab that covers four areas:

1. **Networking** — DNS, filtering, routing, segmentation, remote access
2. **Infrastructure** — Linux administration, containers, service management
3. **Observability** — uptime checks, dashboards, metrics, logs
4. **Self-hosted apps** — storage, utility tools, and internal services

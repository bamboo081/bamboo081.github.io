---
layout: default
title: Home
---

<div class="top-nav">
  <a href="{{ '/' | relative_url }}">Home</a>
  <a href="{{ '/timeline' | relative_url }}">Timeline</a>
  <a href="{{ '/services' | relative_url }}">Services</a>
  <a href="{{ '/troubleshooting' | relative_url }}">Troubleshooting</a>
</div>

# Bamboo Homelab

A public record of my homelab build, testing, self-hosted services, and network experiments.

## Current setup

- **Homelab router:** older Verizon FiOS router dedicated to the lab
- **Laptop:** Lenovo Legion used for administration, testing, remote access, and troubleshooting
- **Desktop:** main homelab machine running Ubuntu and hosting most of the lab work

## What this homelab is for

This lab started as a way to create a separate environment for learning real infrastructure work instead of only running apps on my everyday machines. The main goals have been:

- building a separate networked lab environment
- learning Linux administration on real hardware
- testing remote access and VPN workflows
- hosting services with Docker
- setting up DNS-level filtering and monitoring
- creating a foundation for bigger tools like dashboards, reverse proxies, cloud storage, and automation

## What I have already done

### Network buildout

- repurposed an older FiOS router for homelab use
- separated the lab from the main home network with its own router path
- moved toward a cleaner lab topology where the homelab router acts as the boundary for the lab
- used the laptop and desktop across both local and remote access workflows

### Core system setup

- moved the homelab desktop toward Ubuntu as the main platform
- cleaned up old boot complexity from prior dual-boot / Hackintosh experimentation
- recovered from boot issues by using a stable working kernel when a newer one failed

### Remote access

- installed and used Tailscale on the Ubuntu systems
- tested remote access over both local network paths and Tailscale
- evaluated remote desktop quality and latency between the laptop and the desktop

### Containers and services

- installed or worked on Docker and Docker Compose
- tested Portainer for container management
- started working on Pi-hole for DNS filtering and ad blocking
- explored other services to add next, including monitoring, reverse proxying, and home automation

## Current status

<div class="card-grid">
  <div class="card">
    <h3>Working</h3>
    <ul>
      <li>separate homelab network concept</li>
      <li>Ubuntu homelab machine</li>
      <li>Tailscale connectivity</li>
      <li>basic container stack direction</li>
    </ul>
  </div>
  <div class="card">
    <h3>In progress</h3>
    <ul>
      <li>Pi-hole / DNS filtering</li>
      <li>better remote desktop quality</li>
      <li>service reliability and startup behavior</li>
      <li>monitoring and dashboards</li>
    </ul>
  </div>
  <div class="card">
    <h3>Still being debugged</h3>
    <ul>
      <li>DNS resolution edge cases</li>
      <li>container networking conflicts</li>
      <li>virtualization / KVM issues</li>
      <li>Wi-Fi stability and throughput consistency</li>
    </ul>
  </div>
</div>

## Planned additions

- Uptime Kuma
- Prometheus and Grafana
- Nextcloud
- Home Assistant
- Caddy or Nginx Proxy Manager
- stronger network-level filtering and traffic control

## Recent posts

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}

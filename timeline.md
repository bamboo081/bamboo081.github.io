---
layout: default
title: Timeline
---

<div class="top-nav">
  <a href="{{ '/' | relative_url }}">Home</a>
  <a href="{{ '/timeline' | relative_url }}">Timeline</a>
  <a href="{{ '/services' | relative_url }}">Services</a>
  <a href="{{ '/troubleshooting' | relative_url }}">Troubleshooting</a>
</div>

# Homelab timeline

This is the cleaned public version of the progress so far.

## 1. Starting point

The homelab centered around three pieces of hardware:

- a dedicated homelab FiOS router
- my Lenovo Legion laptop
- my current desktop

## 2. Building a separate lab network

One of the first useful steps was moving from "extra devices on the home network" to a more deliberate lab setup.

What changed:

- an older Verizon FiOS router was reused for the homelab
- the homelab was split from the main house network into its own segment
- the lab machines were moved behind the homelab router instead of being treated as ordinary client devices

Why it mattered:

- easier testing without changing the whole home network
- better isolation for experiments
- a clearer path for self-hosted services and security testing

## 3. Moving the server side onto Ubuntu

The desktop became the main homelab machine.

Work done:

- used Ubuntu as the main OS direction for the lab
- simplified the system after earlier multi-boot and Hackintosh experiments
- recovered from Ubuntu boot issues by using a known-good kernel when a newer kernel produced a black screen

## 4. Remote access and lab management

Once the core machines were in place, the next step was being able to reach them reliably.

Work done:

- installed and used Tailscale
- tested remote access from the Legion laptop to the desktop
- tried both direct local paths and Tailscale-based paths
- compared connection quality and responsiveness

Main lesson:

Remote access can be "working" without being good. Video quality, latency, encoding, and the network path all matter, not just whether a session opens.

## 5. Containerizing the homelab direction

The next phase was moving toward a service-hosting environment.

Work done:

- installed Docker tooling
- used or attempted to use Docker Compose
- brought up Portainer for container management
- started work on Pi-hole for network-wide DNS filtering

This was the point where the lab started turning into more than just a Linux box.

## 6. DNS and filtering experiments

A large part of the current work has been around DNS.

Work done:

- tested Pi-hole deployment
- investigated why IP connectivity worked while domain lookups failed
- found service conflicts around DNS port usage
- adjusted resolver behavior and upstream DNS decisions

Main lesson:

DNS problems can look like "the internet is broken" even when raw network connectivity is perfectly fine.

## 7. Performance and stability testing

The lab also became a place to evaluate general network and system quality.

Areas tested:

- Wi-Fi speed consistency
- remote desktop image quality and lag
- service startup behavior
- virtualization readiness
- router capability and general network bottlenecks

## 8. Next phase

The next stage is turning the lab into a more complete self-hosted environment with:

- uptime monitoring
- dashboards and metrics
- reverse proxying
- cloud-style storage
- home automation integrations
- stronger network filtering and control

---
layout: default
title: Troubleshooting
---

<div class="top-nav">
  <a href="{{ '/' | relative_url }}">Home</a>
  <a href="{{ '/timeline' | relative_url }}">Timeline</a>
  <a href="{{ '/services' | relative_url }}">Services</a>
  <a href="{{ '/troubleshooting' | relative_url }}">Troubleshooting</a>
</div>

# Troubleshooting notes

A large part of this homelab has been learning by breaking things and then figuring out why they failed.

## Ubuntu boot issues

### Problem

A newer kernel booted to a black screen.

### What helped

- booting from an older working kernel
- treating that kernel as the stable fallback while diagnosing the newer one

### Lesson

Do not assume the latest kernel is automatically the best kernel for a given machine.

## DNS failures

### Problem

Basic connectivity worked, but domain names did not resolve.

### What this pointed to

- DNS configuration issues rather than total network failure
- a service conflict or resolver misconfiguration

### Lesson

Always separate these two questions:

- can the machine reach the network?
- can the machine resolve names?

## Port 53 conflicts

### Problem

Pi-hole needed DNS port access, but another service was already using it.

### Why it mattered

A DNS service cannot reliably start if something else already owns the standard DNS port.

### Lesson

Before launching any DNS stack, check which process is already bound to the port.

## Portainer HTTP/HTTPS mismatch

### Problem

Portainer gave an HTTP-to-HTTPS error when opened the wrong way.

### Lesson

Container dashboards often expose different ports for secure and non-secure access. The port and protocol must match.

## Remote desktop quality

### Problem

Remote access technically worked, but the experience was poor: lag, low visual quality, and inconsistent smoothness.

### Likely factors

- encoding method
- client/server desktop stack
- Wi-Fi conditions on the client side
- route taken between devices
- desktop environment overhead

### Lesson

Remote access performance is a full-stack problem, not just a bandwidth problem.

## Virtualization / KVM issues

### Problem

The system did not behave like a clean ready-to-go virtualization host even though that was a desired use case.

### Lesson

Virtualization depends on more than the CPU model. Firmware settings, modules, the active kernel, and service behavior all need to line up.

## Wi-Fi inconsistency

### Problem

Wireless speeds were not stable and could drop much lower than expected.

### Lesson

Throughput problems can come from several layers at once:

- the router
- the radio band in use
- the client device
- interference
- channel width / mode
- ISP plan behavior versus real-world conditions

---
layout: default
title: "Services tested so far and what broke"
---

The container and service side of the homelab has been the most educational part so far.

What I worked on:

- Docker and Docker Compose
- Portainer
- Pi-hole
- Tailscale

What went wrong:

- DNS conflicts
- port usage conflicts
- protocol mismatches when accessing dashboards
- remote desktop quality problems
- virtualization readiness issues

That is normal for a first serious homelab. Most of the value comes from tracing exactly why something failed and then designing the next version more cleanly.

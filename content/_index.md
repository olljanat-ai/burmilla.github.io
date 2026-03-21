---
title: BurmillaOS
layout: hextra-home
---

<div class="hx:mt-6 hx:mb-6">
{{< hextra/hero-headline >}}
  The minimal OS&nbsp;<br class="hx:sm:block hx:hidden" />built for Docker
{{< /hextra/hero-headline >}}
</div>

<div class="hx:mb-12">
{{< hextra/hero-subtitle >}}
  Every process runs as a Docker container.&nbsp;<br class="hx:sm:block hx:hidden" />
  Lightweight, fast, and built to replace RancherOS.
{{< /hextra/hero-subtitle >}}
</div>

<div class="hx:mb-12">
{{< hextra/hero-button text="Quick Start" link="docs/quick-start-guide" >}}
{{< hextra/hero-button text="View Docs" link="docs" style="secondary" >}}
</div>

{{< hextra/feature-grid >}}
  {{< hextra/feature-card
    title="Everything is a Container"
    icon="cube"
    subtitle="System services like ntpd, syslog, and the console all run as Docker containers — no init system, no systemd."
  >}}
  {{< hextra/feature-card
    title="Minimal Footprint"
    icon="chip"
    subtitle="Stripped of everything not needed to run Docker. Starts in seconds and requires as little as 1 GB of RAM."
  >}}
  {{< hextra/feature-card
    title="Dual Docker Design"
    icon="adjustments"
    subtitle="System Docker manages OS services; a separate user Docker handles your workloads — isolated and safe."
  >}}
  {{< hextra/feature-card
    title="Cloud Ready"
    icon="cloud"
    subtitle="Runs on AWS, GCE, Azure, DigitalOcean, OpenStack, VMware ESXi, and more with cloud-config support."
  >}}
  {{< hextra/feature-card
    title="Reduced Attack Surface"
    icon="shield-check"
    subtitle="Fewer components means fewer vulnerabilities. Libraries live inside containers, not on the host."
  >}}
  {{< hextra/feature-card
    title="Latest Docker"
    icon="arrow-circle-up"
    subtitle="Always ships with the latest Docker release so you can take advantage of new capabilities and fixes."
  >}}
{{< /hextra/feature-grid >}}

<div class="hx:mt-12">

## Hardware Requirements

Platform   | RAM
--------   | ---
Baremetal  | 1 GB
VirtualBox | 1 GB
VMware     | 1 GB
GCE        | 1 GB
AWS        | 1 GB

## How It Works

Everything in BurmillaOS is a Docker container. The system launches two Docker instances:

- **System Docker** — the first process on the system, runs all OS-level services (ntpd, syslog, console, udev) as containers. Replaces traditional init systems.
- **User Docker** — a dedicated Docker daemon for your containers, isolated from System Docker so `docker rm -f $(docker ps -qa)` can never wipe the OS.

![How it works](/images/howitworks.png)

## Supported Workloads

BurmillaOS is best suited for:

- Standalone Docker containers (`docker run` / `docker create`)
- Multi-container applications (`docker-compose`)
- Docker Swarm mode (`docker stack deploy` / `docker service`)

> Kubernetes and Rancher 2.x are not the focus of BurmillaOS. Consider [k3OS](https://github.com/rancher/k3os) for those use cases.

## Community

- [GitHub Discussions](https://github.com/burmilla/os/discussions)
- [Discord Server](https://discord.com/invite/AR6daurAAk)
- [Releases](https://github.com/burmilla/os/releases)

</div>

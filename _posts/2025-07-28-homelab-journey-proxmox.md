---
title: "My Homelab Journey: Discovering Proxmox"
date: 2025-07-28T10:00:00+02:00
classes: wide
categories:
  - homelab
tags:
  - beelink
  - szbox
  - ubuntu
  - proxmox
---

After a few months running my small homelab with three Docker Compose stacks on an Ubuntu Desktop machine, I decided to upgrade my setup. I wanted more room to try new things and to encapsulate them into a few virtual machines, so I could delete or restore them individually instead of having all the Docker containers running in the same Ubuntu Desktop environment.

Also, my machine was not quite stable—every few days it would restart itself, and despite checking temps, resources, and system logs, I couldn't find the root cause. I hoped to make my self-hosted services more stable by using Ubuntu Server instead of Desktop.

Finally, my curiosity for new technology led me to [Proxmox](https://www.proxmox.com/en/), which I had been researching for some time. I wanted to try it out as it piqued my interest.

## What is Proxmox?
[Proxmox](https://www.proxmox.com/en/) is an open source platform for enterprise virtualization. They offer:
- [Proxmox Virtual Environment](https://www.proxmox.com/en/products/proxmox-virtual-environment/overview)
- [Proxmox Backup Server](https://www.proxmox.com/en/products/proxmox-backup-server/overview)
- [Proxmox Mail Gateway](https://www.proxmox.com/en/products/proxmox-mail-gateway/overview)

I will only cover the Virtual Environment, as I don't yet have a NAS for VM backups or disks. As always, it's best to start small and expand later.

## Installing Proxmox
- [Proxmox download page](https://www.proxmox.com/en/downloads)
- [Installation guide (YouTube)](https://www.youtube.com/watch?v=sZcOlW-DwrU) by [CraftComputing](https://www.youtube.com/@CraftComputing)
- [Proxmox helper scripts video](https://www.youtube.com/watch?v=kcpu4z5eSEU) by [TechnoTim](https://www.youtube.com/@TechnoTim)
- [Proxmox helper scripts](https://community-scripts.github.io/ProxmoxVE/scripts) by the Proxmox Community

**Quick tips:**
- Use a tool like [Rufus](https://rufus.ie/en/) or [WinSetupFromUSB](https://winsetupfromusb.org/) to burn the Proxmox ISO to a USB drive.
- Boot from the USB and install Proxmox as you would any OS. I only changed a couple of options based on the video guides above.
- While you have a keyboard and mouse connected, enable automatic restart after power loss in the BIOS, very useful for homelab uptime!

## Hardware Research & Purchase
![Here we go again meme from GTA]({{ site.url }}{{ site.baseurl }}/assets/images/posts/2025-07-28-homelab-journey-proxmox/HereWeGoAgain.png)

Here we go spending money again. This hobby gets more expensive!

One of the coolest features of Proxmox is clustering. With at least three physical machines in a cluster, you can enable [HA (High Availability)](https://pve.proxmox.com/wiki/High_Availability) for VMs. This means:
- You can migrate any VM or LXC container from one host to another (the VM/LXC must be stopped for migration).
- With HA, this process is automated: if a host goes down, another host takes over its VMs.

I wanted to future-proof my homelab for when I eventually buy a house. My goal: a 3-node cluster with HA and Home Assistant.

### My Hardware Journey
- **First node:** [Beelink SER5 mini PC](https://www.bee-link.com/), AMD 5800U (6 cores, 12 threads), 16GB RAM. I loved the low power consumption and performance.
- **New nodes:** After research, I found the [Ryzen 7 7730U](https://en.wikipedia.org/wiki/List_of_AMD_Ryzen_processors) (8 cores, 16 threads, Vega 8 GPU, 15W TDP). I found [SZBOX Ryzen 7 7730U mini PCs](https://es.aliexpress.com/item/1005007536343635.html?spm=a2g0o.order_detail.order_detail_item.3.25dc39d3eZ56lF&gatewayAdapt=glo2esp) on AliExpress, bought two barebones units (no RAM/SSD/OS) for under 200€ each with a coupon. I added 32GB RAM and a 1TB M.2 SSD to each, totaling about 700€ for both.

## Cluster Setup & Current State
I am missing a key piece for my homelab: a NAS, to complete the Proxmox cluster and achieve its full potential.

- The two new mini PCs run Proxmox and are in the same cluster.
- The old Beelink mini PC remains as the media server (Ubuntu Desktop).
- I migrated services like RustDesk, WireGuard, AdGuard Home, Portainer, Homepage, and Nginx Proxy Manager to the Proxmox cluster.

### Future Plans
I have already ordered a [Beelink ME mini 6-Slot](https://www.bee-link.com/products/beelink-me-mini-n150?variant=47599172813042) as my NAS. Once it arrives, I plan to:
- Install TrueNAS as the OS
- Move the media server stack to the NAS
- Reformat the old Beelink as a Proxmox node to join the cluster
- Enable automatic VM backups
- Move VM disks to NAS so that I can enable High Availability 

## Proxmox for Unreal Engine: Horde Build Farm
A very cool addition: I now run an [Unreal Engine Horde](https://dev.epicgames.com/documentation/en-us/unreal-engine/horde-in-unreal-engine) server. I have the main Horde server and two agents to help with local C++ builds and compilation. While not always needed for small changes, it's a huge time saver for full engine upgrades or large code changes.

I will explain my Unreal Engine Horde setup in more detail in a future post.
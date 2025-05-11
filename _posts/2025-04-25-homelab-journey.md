---
title: "My Homelab Journey: From Docker Curiosity to a Full-Fledged Home Server"
date: 2025-04-25T10:00:00+02:00
classes: wide
categories:
  - homelab
  - linux
  - docker
  - self-hosting
tags:
  - beelink
  - ubuntu
  - jellyfin
  - home-assistant
  - rustdesk
  - syncthing
  - portainer
  - heimdall
---

## From Work Curiosity to Home Lab

As I dabbled with [Docker](https://www.docker.com/) at work, specifically for [Unreal Engine](https://www.unrealengine.com/) Linux dedicated servers, I found myself wanting to experiment more with technology at home.

## Hardware & Setup

That curiosity led me to purchase a [Beelink SER5 mini PC](https://www.bee-link.com/), featuring an AMD 5800U (6 cores, 12 threads) and 16GB of RAM. I added a new 2TB internal SSD for extra storage and installed [Ubuntu Desktop](https://ubuntu.com/desktop) on it, setting up a dual boot with Windows on the original drive and Linux on the new one.

To make the setup more robust, I tweaked the BIOS:
- Enabled automatic power-on after power loss
- Enabled Wake-on-LAN for remote starts

## First Experiments: Emulation

With my Ubuntu box now always available in the living room (connected to the TV), I started by installing some emulators. It was great to play my old Game Boy Advance games from the comfort of the sofa, though I did run into some driver issues with my Xbox One controller (it is Linux after all).

## Entering the World of Homelab

Looking for more challenges, I dove into the world of homelabbing. Within a few days, I had three Docker Compose stacks running:

1. **RustDesk Server Stack:** Running a [RustDesk](https://rustdesk.com/) relay server, an open-source alternative to TeamViewer or Parsec that works wonderfully for remote access.
2. **Main Homelab Stack:** Hosting [Home Assistant](https://www.home-assistant.io/), a [WireGuard VPN](https://www.wireguard.com/), [Portainer](https://www.portainer.io/) for container management, [Heimdall](https://heimdall.site/) as a homepage for all my services, and [Syncthing](https://syncthing.net/) to sync files between my main PC and the mini PC.
3. **Media Server Stack:** Running several [*arr](https://trash-guides.info/) applications and a [Jellyfin](https://jellyfin.org/) server to watch my shows and films.

I opened up some ports on my router and configured my domain with [Cloudflare](https://www.cloudflare.com/), so I can access my Jellyfin server from outside my home.

## Automation & Maintenance

To keep everything up to date, I wrote a cron job that runs a shell script to automatically update all three Docker Compose stacks. After a few days, I added another script to prune old Docker images, since they started piling up and consuming a lot of disk space.

## Reflections

This journey has been a fun and rewarding way to learn more about Linux, Docker, and self-hosting. I'm afraid that as I love playing around with all these things, I am going to enter a deep rabbit hole for at least some months. Let's see where I end up one or two years from now!

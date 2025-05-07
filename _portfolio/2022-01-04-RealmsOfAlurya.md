---
title: "Realms of Alurya"
classes: wide
author_profile: false
order: 7
excerpt: "Comercial UE5 third person arpg. Diablo like combat and dungeons. Nfts and blockchain."
header:
  teaser: /assets/images/portfolio/2022-01-04-RealmsOfAlurya/RealmsOfAlurya.png
sidebar:
  - title: ""
    image: /assets/images/portfolio/2022-01-04-RealmsOfAlurya/RealmsOfAlurya.png
    image_alt: "Realms Of Alurya image" 
  - title: "Date"
    text: "2022 - Current"
  - title: "Company"
    text: "[Synergy Games](https://www.synergygames.es/)"
  - title: "Role"
    text: "Senior UE generalist programmer."
  - title: "Webpage"
    text: "[Realms Of Alurya](https://www.realmsofalurya.com/)"
  - title: "Platforms / Stores"
    text: "[Propietary Launcher](https://installer.launcher.xsolla.com/xlauncher-builds/xsolla-launcher-update/12388/bin/installer.exe)<br>[Epic Games](https://store.epicgames.com/en-US/p/realms-of-alurya-0ad02f?lang=en-US)<br>[Steam](https://store.steampowered.com/app/3500760/Realms_of_Alurya/)"
gallery:
  - url: /assets/images/portfolio/2022-01-04-RealmsOfAlurya/RealmsOfAlurya.png
    image_path: assets/images/portfolio/2022-01-04-RealmsOfAlurya/RealmsOfAlurya.png
    alt: "Realms Of Alurya image"
  - url: /assets/images/portfolio/2022-01-04-RealmsOfAlurya/001.jpg
    image_path: assets/images/portfolio/2022-01-04-RealmsOfAlurya/001.jpg
    alt: "Realms Of Alurya image"
  - url: /assets/images/portfolio/2022-01-04-RealmsOfAlurya/006.jpg
    image_path: assets/images/portfolio/2022-01-04-RealmsOfAlurya/006.jpg
    alt: "Realms Of Alurya image"
  - url: /assets/images/portfolio/2022-01-04-RealmsOfAlurya/014.jpg
    image_path: assets/images/portfolio/2022-01-04-RealmsOfAlurya/014.jpg
    alt: "Realms Of Alurya image"
  - url: /assets/images/portfolio/2022-01-04-RealmsOfAlurya/NftDashboard.png
    image_path: assets/images/portfolio/2022-01-04-RealmsOfAlurya/NftDashboard.png
    alt: "Nft Dashboard image"
  - url: /assets/images/portfolio/2022-01-04-RealmsOfAlurya/BuildManager.png
    image_path: assets/images/portfolio/2022-01-04-RealmsOfAlurya/BuildManager.png
    alt: "Build Manager image"
---

<p align='justify'>SynergyLand is my second commercial game and my role has been as a generalist senior programmer.<br><br>
Synergy Land is an Action RPG game that integrates MOBA mechanics into a player-driven world that allows players real ownership of digital game assets. It has been developed with Unreal Engine 5.<br><br>
I have designed and developed the game core systems from simple widget blueprints to managers to handle the communication with the Playfab/Azure cloud solutions.<br><br>
A lot of my time has been working hand to hand with our backend engineer, as I handle almost everything related to the client and game servers communication with our backend services. I find these long talks very interesting as I can learn about his needs for the backend while I help him learn how our Unreal client and server architecture works.<br><br>
Another of my responsibilities has been build generation and deployment to XSolla. To automate the process while we don't have a build server to setup any CI/CD, I have created an <a href="https://www.autohotkey.com/">AutoHotKey</a> script that generates UnrealHeaderTools bats, setups variables in config files, creates zips of the builds, signs the client executables and can update the playfab fleets while cleaning up the old versions automatically. This way we generate manual builds on specific days but the process is much easier and less error-prone.<br><br>

As I love fiddling around and trying technologies some of the tools or works that I am most proud would be:</p>

<ul align='justify'>
<li>Help an animator by creating a python script to rebuild an Autodesk Maya animation plugin json database, as sometimes it started going haywire and missing elements.</li>
<li>Create a base item editor widget editor blueprint making it easier and more visual while managing game items as they were starting to get quite complex.</li>
<li>Create an in-game admin panel, and cheat component enabled only on non-shipping builds with a lot of cheats to easily debug and speed up the game.</li>
<li>Created an editor module and added some buttons in the unreal editor toolbar in order to rebuild our Island game mode map, as it is a cluster of many islands and has to be configured in a certain way to maintain crossreferences between the actors. Before this automation this process took a long time and a lot of times we had human errors.</li>
<li>First I made a bunch of python scripts to create testing Nfts on our Dev environment. Then I made an upgrade by creating an executable app based in react and electron, so any employee could give themselves or other persons testing Nfts, currencies, unlocks, etc. that are stored in the backend without the need of any technical skill or software requirement.</li>
</ul><br>

<p align='justify'>I also am in duty of mantaining the Plastic repository and help other team members when problems occur.<br><br>
By using the Playfab and Azure ecosystem with linux dedicated servers inside docker images, we are able to have a base of a closs-platform game ready with easy scalability and regions expansion. This way in the future when we expand to other platforms the users will be able to play together.</p>

### Azure technologies used:
- [Azure](https://azure.microsoft.com/en-us/) as the main cloud based solutions.
- [Playfab](https://playfab.com/) in order to host our game servers and player accounts.
- [Blob Storage](https://azure.microsoft.com/en-us/products/storage/blobs) to store our game server logs, and player persistence with backups.
- [PubSub Service](https://azure.microsoft.com/en-us/products/web-pubsub) to have realtime connection the unreal game clients and dedicated servers.
- [App Service](https://azure.microsoft.com/en-us/products/app-service) to host our backend segregated between multiple app service instances.
- [Microsoft Entra ID](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-id) to provide access and configure permissions to employees.
- [Virtual Machines](https://azure.microsoft.com/en-us/products/virtual-machines) to setup other services.

### Other technologies used:
- [MongoDB](https://www.mongodb.com/) as the main backend database.
- [CircleCI](https://circleci.com/) to monitor backend deployments.
- [Xsolla](https://xsolla.com/) as our custom launcher.
- [Bugsplat](https://www.bugsplat.com/) crash and error reporting.
- [Plastic SCM](https://www.plasticscm.com/) as our vcs.

### Gallery
{% include gallery layout="third" %}

### Trailer
{% include video id="weXDa10ZPr8" provider="youtube" %}
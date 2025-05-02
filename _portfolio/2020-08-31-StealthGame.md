---
title: "Stealth Game"
classes: wide
author_profile: false
order: 4
excerpt: "UE4 Multiplayer Udemy project. Basic replication introduction."
header:
  teaser: /assets/images/portfolio/2020-08-31-StealthGame/StealthGame.png
sidebar:
  - title: ""
    image: /assets/images/portfolio/2020-08-31-StealthGame/StealthGame.png
    image_alt: "Stealth Game image" 
  - title: "Date"
    text: "2020"
  - title: "Repository"
    text: "[Gitlab](https://gitlab.com/alfred632/unreal_tutorials)"
  - title: "Udemy course"
    text: "[Unreal Course](https://www.udemy.com/course/unrealcourse/)"
  - title: "Download"
    text: "[Zip](https://mega.nz/file/ppARAIpJ#GnTk9Jkvb1wmM5rS16go3L4aCj0Cv--VyX-f0HFiTuc)"
gallery:
  - url: /assets/images/portfolio/2020-08-31-StealthGame/StealthGame.png
    image_path: assets/images/portfolio/2020-08-31-StealthGame/StealthGame.png
    alt: "Stealth Game image"
---

<p align='justify'>
This time was a small project but with a twist of multiplayer.<br><br>
The game is fairly simple. We have a AI guard with its BT that can patrol. If any guard sees any player, you lose the game.<br>
The objective is to retrieve the mission object and go to the escape zone with it without any guard seeing you.
The guards are equipped with the PawnSensing component but you can distract them with your gun, you only have to shoot and they will investigate the noise of the projectile.<br><br>
The multiplayer aspect consists on activating replication of actors, and replicate some custom C++ variables that have OnRep functions to update the clients.</p><br>
<p>This tutorial also had 2 fun little challenges:</p>
<ul>
<li>A jumpad that launches the actor flying in a direction.</li>
<li>A black hole that attracts and destroys actors that have physics enabled.</li>
</ul>

{% include gallery layout="one" %}

### Gameplay showcase
<div class="video-container">
  <iframe src="https://mega.nz/embed/hsBEHYgS#3Ojw3iB7Ev4ZyOE393q4biuG-Vi-DoAXZOc7y1hwV64" 
          frameborder="0" 
          allowfullscreen>
  </iframe>
</div>

### Extra: Tutorial challenge
<div class="video-container">
  <iframe src="https://mega.nz/embed/4oJzWKII#2JUcjf-veKBt0roUfS68UNx3tD00Yp0Eh4wvV3-NJME" 
          frameborder="0" 
          allowfullscreen>
  </iframe>
</div>
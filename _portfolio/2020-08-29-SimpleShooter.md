---
title: "Tutorial: Simple Shooter"
classes: wide
author_profile: false
order: 3
excerpt: "UE4 Singleplayer Udemy project. Basic unreal game loop. Main menu, settings, win/loose conditions."
header:
  teaser: /assets/images/portfolio/2020-08-29-SimpleShooter/SimpleShooter.png
sidebar:
  - title: ""
    image: /assets/images/portfolio/2020-08-29-SimpleShooter/SimpleShooter.png
    image_alt: "Simple Shooter image" 
  - title: "Date"
    text: "2020"
  - title: "Repository"
    text: "[Gitlab](https://gitlab.com/alfred632/unreal_tutorials)"
  - title: "Udemy course"
    text: "[Unreal Course](https://www.udemy.com/course/unrealcourse/)"
  - title: "Download"
    text: "[Zip](https://mega.nz/file/t5QGFYTK#16DU86bJRDVnBRoUQO8l7ZrYs96eATiTZAhKPT375_c)"
gallery:
  - url: /assets/images/portfolio/2020-08-29-SimpleShooter/SimpleShooter.png
    image_path: assets/images/portfolio/2020-08-29-SimpleShooter/SimpleShooter.png
    alt: "Simple Shooter image"
---

This was my second project using the Unreal Engine.  

You are a character that has infiltrated a base and needs to kill all the enemies. If you kill them all you win, if you die you lose.  

This time I tackled more systems and components than the last game:
- Made a GameMode for the first time that handles the win/lose conditions and restarts the level.
- Made a gun that shoots using the LineTrace physics API of Unreal.
- Used Behaviour Trees and Blackboards for the first time in Unreal.
- Also implemented custom Tasks and Services for the BT in C++.  

When I finished the tutorial I wanted to expand the project a bit more, so I made the following upgrades:
- Made a new gun that launches projectiles and applies a radial damage.
- Implemented a weapon switching system so we can play with all of them.
- Added ammo and reload to the weapons and UI.
- Made the weapons dropped from the enemies to give ammo who runs over them.
- Up & Down arrows modify the mouse sensitivity.
- Finally, made a Main Menu with a settings panel to modifiy resolutions, maximised windows or fullscreen and FPS limiter.  

I found interesting how Unreal Engine has already a game framework setup with base classes like the game mode, game state, player controller, player state, pawn, hud, game instance, etc. Coming from my custom engine and some small Unity projects this was quite puzzling and complex at first, but in the end I liked how it was structured.  

### Gallery
{% include gallery layout="one" %}

### Gameplay showcase
<div class="video-container">
  <iframe src="https://mega.nz/embed/5pJiRSaY#gSDBs4cFsZglBFQ_j0ZXaBpS4ucE6NorQJ3PKb_H_W4" 
          frameborder="0" 
          allowfullscreen>
  </iframe>
</div>
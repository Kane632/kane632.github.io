---
title: "Those Who Came"
classes: wide
author_profile: false
order: 6
excerpt: "Comercial UE4 third person arpg. Better with friends!"
header:
  teaser: /assets/images/portfolio/2021-01-12-ThoseWhoCame/ThoseWhoCame.png
sidebar:
  - title: ""
    image: /assets/images/portfolio/2021-01-12-ThoseWhoCame/ThoseWhoCame.png
    image_alt: "Those Who Came image" 
  - title: "Date"
    text: "2021 - 2022"
  - title: "Company"
    text: "[RolldBox](https://rolldbox.com/)"
  - title: "Role"
    text: "Mid UE generalist programmer."
  - title: "Webpage"
    text: "[Those Who Came](https://thosewhocame.com/)"
  - title: "Platforms / Stores"
    text: "[Steam](https://store.steampowered.com/app/1708570/Those_who_Came/)"
gallery:
  - url: /assets/images/portfolio/2021-01-12-ThoseWhoCame/ThoseWhoCame.png
    image_path: assets/images/portfolio/2021-01-12-ThoseWhoCame/ThoseWhoCame.png
    alt: "Those Who Came image"
  - url: /assets/images/portfolio/2021-01-12-ThoseWhoCame/BuildManager.png
    image_path: assets/images/portfolio/2021-01-12-ThoseWhoCame/BuildManager.png
    alt: "Build Manager image"
---

<p align='justify'>
This is my first commercial game and my role has been almost as of the lead programmer because in the span of two years two programmers came and went and I was the only that started and ended the project.<br><br>

This game is a multiplayer 3rd person, sci-fi, coop RPG game where the more friends play together, more synergies appear between the energies available! You must solve puzzles and heal the planet Solarus. It has been developed with Unreal Engine 4.<br><br>

I have designed and developed the game core systems from simple widget blueprints to managers to handle the communication with the AWS cloud solutions.<br><br>

Another of my responsibilities has been build generation and deployment to Steam. To automate the process while we don't have a dedicated build server and setup any CI/CD like Jenkins, I have created an <a href="https://www.autohotkey.com/">AutoHotKey</a> script that generates UnrealHeaderTools bats, setups variables in .ini and .cs files, creates zips of the builds and uploads debug symbols to Bugsplat automatically. This way we generate manual builds on specific days but the process is much easier and less error-prone.</p>

<p align='justify'>
I also am in duty of mantaining the Git repository and help other team members when problems occur.<br><br>
By using the Amazon Web Services ecosystem with linux dedicated servers we are able to have the base of a closs-platform and scalable game ready with our custom friends and party system. This way in the future when we expand to other platforms the users will be able to play together.</p>

### AWS technologies used:
- [Gamelift](https://aws.amazon.com/gamelift/) as the main cloud provider.
- [Cognito](https://aws.amazon.com/cognito/) for account creation and management.
- [DynamoDB](https://aws.amazon.com/dynamodb/) as the main database.
- [API Gateway](https://aws.amazon.com/api-gateway/) to route our lambda functions and matchmaking events.
- [Lambda](https://aws.amazon.com/lambda/) to host our backend as serverless code.
- [Cloudwatch](https://aws.amazon.com/cloudwatch/) to store and monitor service logs.

### Gallery
{% include gallery layout="half" %}

### Trailer
{% include video id="iVGxNepjp8k" provider="youtube" %}
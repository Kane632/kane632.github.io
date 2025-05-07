---
title: "Tool: ScreenDeck"
classes: wide
author_profile: false
order: 8
excerpt: "Customizable Stream Deck-like tool for Windows, built with AutoHotKey. Touchscreen support, flexible profiles, and open scripting."
header:
  teaser: /assets/images/portfolio/2024-12-26-ScreenDeck/ScreenDeck_1.png
sidebar:
  - title: ""
    image: /assets/images/portfolio/2024-12-26-ScreenDeck/ScreenDeck_1.png
    image_alt: "ScreenDeck UI example"
  - title: "Date"
    text: "2024"
  - title: "Repository"
    text: "[GitHub](https://github.com/Kane632/ScreenDeck)"
  - title: "Platform"
    text: "Windows ([AutoHotKey v2.0](https://www.autohotkey.com/))"
gallery:
  - url: /assets/images/portfolio/2024-12-26-ScreenDeck/ScreenDeck_1.png
    image_path: assets/images/portfolio/2024-12-26-ScreenDeck/ScreenDeck_1.png
    alt: "ScreenDeck profile 1 UI example"
  - url: /assets/images/portfolio/2024-12-26-ScreenDeck/ScreenDeck_2.png
    image_path: assets/images/portfolio/2024-12-26-ScreenDeck/ScreenDeck_2.png
    alt: "ScreenDeck profile 2 UI example"
  - url: /assets/images/portfolio/2024-12-26-ScreenDeck/ScreenDeck_3.png
    image_path: assets/images/portfolio/2024-12-26-ScreenDeck/ScreenDeck_3.png
    alt: "ScreenDeck folders UI example"
---

<p align="justify">
ScreenDeck is a fully customizable Stream Deck-like tool for Windows, designed for use with any touchscreen (but a mouse works too). Built with AutoHotKey, it allows users to create as many profiles as needed, each with unique icons, texts, colors, and actions. Unlike commercial solutions, ScreenDeck is open and scriptable so users can define their own functions and automate any workflow they want.
</p>

## Key Features
- Touchscreen support: Use any external touchscreen as your deck.
- Unlimited profiles: Organize actions by context, project, or workflow.
- Customizable UI: Change button size, margins, colors, and more via JSON config.
- Flexible actions: Launch programs, switch profiles, run custom scripts, and more.
- Open scripting: Extend functionality by writing your own functions with the powerful AutoHotKey language.
- Remembers window position and size between sessions.

## Getting Started
1. Download and install [AutoHotKey v2.0](https://www.autohotkey.com/).
2. Run the `ScreenDeck.ahk` script, or use the precompiled executable if available.
3. On first run, a `ScreenDeck.json` config file is generated. Move and resize the UI as needed.
4. Configure your deck by editing the JSON file:
   - Set global UI options in `GuiConfig`.
   - Define multiple `Profiles` with their own actions and appearance.
   - Assign actions to buttons, including launching programs, switching profiles, or running custom scripts.

## Example Configuration
```json
"GuiConfig": {
    "DeckBackgroundColor": "1e7e1b",
    "DeckButtonMargin": 6,
    "DeckButtonSize": 95,
    "ShowTopBar": 0,
    "TopBackgroundColor": "657287"
},
"Profiles": {
    "_Default": {
        "Actions": {
            "0": { "Profile": "Secondary", "Text": "Profile\nWork\nSecondary" },
            "1": { "Action": "OpenPersonalFolder", "Icon": "Folders/W11_yellow.png" }
        }
    },
    "Secondary": { ... }
}
```

## Troubleshooting Touch Input
If touch input is misaligned on multi-monitor setups, calibrate your screens via Windows Control Panel > Tablet PC Settings.

## Project Structure
- `ScreenDeck.ahk`: Main entry point.
- `CustomFunctions.ahk`: Add your own button actions here.
- `GUI.ahk`, `CoreFunctions.ahk`, `CommonFunctions.ahk`: Core logic and helpers.
- `Images/`: Default icons and graphics.
- `lib/`: JSON and GIF libraries for AHK.

## Why ScreenDeck?
ScreenDeck is ideal for power users, streamers, and developers who want a flexible, scriptable, and cost-effective alternative to commercial macro pads. With full control over the UI and logic, you can automate anything on your PC with a simple touch.

## Next steps
You can find more information In the [GitHub](https://github.com/Kane632/ScreenDeck) repository, even contribute to it making it better!

### Gallery
{% include gallery layout="third" caption="Here you can find some examples of my current profiles for home and work." %}

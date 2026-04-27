# ATF MutationStation

![Latest release](https://img.shields.io/github/v/release/Dteyn/ATFMutationStation?include_prereleases)
![Downloads](https://img.shields.io/github/downloads/Dteyn/ATFMutationStation/total)

![ATF MutationStation screenshot](https://github.com/Dteyn/ATFMutationStation/blob/main/assets/images/screenshot.jpg)


**ATF MutationStation** adds new options for creating Mutator Runs in After the Fall VR, allowing you to play **any mutator on any level at any time**, instead of being restricted to only the 'current' mutator.

Both **PCVR** versions are supported (Steam and Oculus Rift). The plugin does not support Meta Quest, Pico, and PSVR -- however, players on those platforms **can** join runs created with ATFMutationStation.

> [!IMPORTANT]
> This plugin is currently in **Beta** status. If you run into any issues, please open an [Issue](https://github.com/Dteyn/ATFMutationStation/issues) or DM me on Discord so issues can be fixed.


# Table of Contents

* [Disclaimer](#disclaimer)
* [Installation Instructions](#installation-instructions)
* [How to Use ATFMutationStation](#how-to-use-atfmutationstation)
* [Troubleshooting](#troubleshooting)
* [Feedback & Support](#feedback--support)



# Disclaimer

> [!WARNING]
> Use at your own risk!!

Generally speaking, After the Fall has not been hostile towards players using BepInEx plugins such as this, so it's commonly accepted to be safe practice as of this plugin's release. In other words, you are unlikely to be banned for using this - **but there are no guarantees**.

While I've made every effort to test this plugin and ensure it's free from bugs and issues, I provide no warranty or guarantees against any issues you may encounter. ___Use at your own risk.___


# Installation Instructions

## Compatibility

* Compatible with **After the Fall** version **1.9.41947** (aka "Nightfall Update").
* Tested and working on **PCVR** (both Steam and Oculus Rift versions).
* **Not compatible** with Meta Quest, Pico, or PSVR versions.

>[!TIP]
> While ATFMutationStation only supports PCVR version, **players on all platforms <ins><i>are able to join</i></ins> runs created with ATFMutationStation!**
>
> As long as a PCVR player running ATFMutationStation creates the party, any other players can join in the fun!

### Other Plugins
As far as I'm aware, ATFMutationStation has no conflicts with any other plugins, and can be used alongside other plugins without issue. If you discover any conflicts, please open an [Issue](https://github.com/Dteyn/ATFMutationStation/issues) with relevant details.



## Installing

**Download and Install**

Use the Full Version .zip below if you are installing After the Fall plugins for the first time. The full version .zip already includes **BepInEx** (version `6.0.0-pre.2`) already within the .zip and is pre-configured, ready to go.

   1.  Grab the latest **`ATFMutationStation-vX.X.X-full.zip`** from the [Releases](https://github.com/Dteyn/ATFMutationStation/releases) section.
   
   2. Extract the .zip file to your After the Fall game folder:

      * **Steam default location:** `C:\Program Files (x86)\Steam\steamapps\common\After The Fall`

      * **Rift default location:** `C:\Program Files\Oculus\Software\Software\vertigo-games-snowbreed`  

After extracting, launch the game. You now have new mutator controls in the 'Mutator Run' screen on the enlisting machines in the lobby.

> [!NOTE]
> **On first launch, startup will take a bit longer than normal** as BepInEx does some initial setup. Subsequent launches will not have this delay.


**Plugin-Only Version**

If you already have BepInEx installed, you can find the .dll only on the releases page. Download the appropriate .zip and extract it to `BepInEx\plugins` in your After the Fall game folder.


## Upgrading

If you are upgrading from an earlier beta of ATF MutationStation - and don't use any other plugins - fully removing the old version is recommended. The previous version used BepInEx `6.0.0-pre.1` and the current version uses BepInEx `6.0.0-pre.2` for improved runtime support.

> [!WARNING]
> If you are using other After the Fall plug-ins that still use BepInEx `6.0.0-pre.1`, they will not work with `6.0.0-pre.2`. In that case, you should stick with version `6.0.0-pre.1`. You can find a .dll of ATF MutationStation compiled for BepInEx `6.0.0-pre.1` on the releases page.

Follow these steps to upgrade to a newer version of ATF MutationStation:

   1. Fully uninstall the old version by removing these folders and files from your After the Fall folder:
      - `\BepInEx\` (and all files within)
      - `\mono\` (and all files within)
      - `.doorstop_version`
      - `changelog.txt`
      - `doorstop_config`
      - `winhttp.dll`

   2. Grab the latest **`ATFMutationStation-vX.X.X-full.zip`** from the [Releases](https://github.com/Dteyn/ATFMutationStation/releases) section.
      
   3. Extract the .zip file to your After the Fall game folder. This will install the latest version.

That's it! You're now upgraded to the latest version of ATF MutationStation. Note that the same delayed startup applies on first launch as BepInEx does initial setup.

> [!TIP]
> As of release v0.5.0, all mutator controls are in-game and the .cfg file is only used for persistence. The GUI app 'ATF MutationStation Manager' previously used with v0.3.0 is no longer required and can be removed.



## Uninstallation

To disable or remove ATF MutationStation, you can use any of these methods:

* **Remove Plugin Only:** Delete `ATFMutationStation.dll` from `BepInEx/plugins`. This will remove ATFMutationStation and leave other plugins intact. Instead of deleting the .dll, you can also create a new folder, `BepInEx/plugins-disabled` and move any plugins you wish to disable into that folder, then move back later to re-enable them.

or

* **Disable BepInEx Entirely:** Rename `winhttp.dll` in the After the Fall folder to something different, like `winhttp-disabled.dll`. This will disable BepInEx entirely including all plugins. Rename back to `winhttp.dll` to re-enable.

or

* **Complete Removal:** To uninstall **everything**, remove these folders and files from your After the Fall folder. After removing these, you are back to stock ATF with nothing installed.
   - `\BepInEx\` (and all files within)
   - `\dotnet\` and/or `\mono\` (and all files within)
   - `.doorstop_version`
   - `changelog.txt`
   - `doorstop_config`
   - `winhttp.dll`



# How to Use ATFMutationStation

Once ATFMutationStation is installed, there will be new controls on the Mutator Run menu on the lobby enlisting machines:

![ATF MutationStation screenshot](https://github.com/Dteyn/ATFMutationStation/blob/main/assets/images/screenshot-circled.jpg)

With these added controls, you can now:

- **Select a Mutator Package** by using the **'Next/Prev'** arrows in the top right corner. Mutator details will update as you page through the 5 available packages.

- **Select a Mutator Level** by using the **'Select Level'** button and choosing a level.

 Simply pick your preferred mutator and level, start the run, and have fun! :)



## Mutator Packages

By default, ATF has five "Mutator Packages". Each package has 3 individual "mutator effects":

### Speed Runner
* **Time Trial**: 15 Minutes to Complete the Run
* **Dry Season**: Health Can No Longer Be Restored
* **Sleight Of Hand**: Advanced Reload Only

### Gun Slinger
* **Sleight Of Hand**: Advanced Reload Only
* **Ammo Shortage**: Max Ammo is Halved
* **Berserk**: Snowbreed Deal Double Damage

### Snapping Turtle
* **Ice Plating**: Snowbreed Have 100% Armor
* **Low Profile**: Snowbreed Crawl Instead of Walk
* **Case Hardened**: Snowbreed Take No Explosive Damage

### Crowd Control
* **Ice Plating**: Snowbreed Have 100% Armor
* **Infestation**: 50% Increase in Snowbreed Spawn Rate
* **Tough Skin**: Snowbreed Health is Doubled

### Snow Plow
* **Motor Function**: Snowbreed can only be killed with Headshots
* **Evolution**: Snowbreed do not Mutilate or Stagger
* **Cold Feet**: Movement Speed is Halved



# Troubleshooting

If something goes wrong, check the logs for signs of troubles:

* **BepInEx log:** `BepInEx\LogOutput.log` (within game folder)

* **ATF's Player.log:** `%LocalAppData%\Vertigo Games\AfterTheFall\Player.log`

For live BepInEx logging, you can also edit `BepInEx\config\BepInEx.cfg` find `[Logging.Console]` and set `Enabled=true` which enables the BepInEx console.

If you run into any issues, please open an [Issue](https://github.com/Dteyn/ATFMutationStation/issues) with detailed feedback on what the issue is and how it can be replicated.



# Feedback & Support

Got issues, suggestions, or questions? The best way to contact me is to open an [Issue](https://github.com/Dteyn/ATFMutationStation/issues), or reach out to me directly on Discord. I often frequent the [After the Fall Discord](https://discord.gg/afterthefall) under my nickname, Dteyn.



## Shout-Outs

### [Astienth](https://github.com/Astienth)

My good friend **Astienth** makes some amazing VR stuff that you must check out!

He has made tons of **bHaptics** and **ProVolver** implementations, including a [bHaptics implementation for ATF](https://github.com/Astienth/AftertheFall_bHaptics) and a [ProVolver implementation for ATF](https://github.com/Astienth/AfterTheFall_Provolver). Give them a try if you have haptic gear!

Astienth also makes a ton of great **flat2VR** conversions, adding VR support to many flatscreen games. Be sure to check out his list of projects on his GitHub page!

- [github.com/Astienth](https://github.com/Astienth)


### [farmertrueVR](https://www.farmertrueVR.com)

My good friend **farmertrue** is a variety VR streamer who streams a wide range of VR content at the highest level possible.

He has a true passion for VR, and gives his honest opinion unlike so many other creators these days. He often streams the latest VR games, and if there is a bHaptics plugin available, you can be certain he'll be using it.

Farmertrue also has a great 18+ Discord community, where we chat about VR on a daily basis, help users with PCVR builds or troubleshooting, and generally just chill out and have a great time hanging in VR. 

Be sure to check him out if you're looking for the best in VR entertainment and information!

- [www.farmertruevr.com](https://www.farmertrueVR.com)
- [twitch.tv/farmertrue](https://twitch.tv/farmertrue)
- [youtube.com/@farmertrueVR](https://youtube.com/@farmertrueVR)
- [Join the farmertrueVR Discord](https://discord.gg/SpKY7ySjXX)


### [Vertigo Games](https://www.vertigo-games.com/)

[After the Fall VR](https://www.afterthefall-vr.com/) was developed by [Vertigo Games](https://www.vertigo-games.com/), a Dutch game developer renowned for their expertise in creating high-quality virtual reality experiences.

In addition to *After the Fall VR*, they are also known for great titles like *Thief VR: Legacy of Shadow*, *Metro: Awakening*, *The 7th Guest VR*, and the *Arizona Sunshine* series, all of which have received high accolades.

A big shout-out and heartfelt thanks to Vertigo Games for making After the Fall such an amazing experience that stands the test of time. The technical work put into the game engine is also an absolute marvel. I'm a huge fan of your work in every aspect!

<sub><i>PS: Please make an After the Fall 2! :)</i></sub>



## About Me

### ATF Projects

I have some other ATF projects listed on my GitHub page - check them out here: 

#### [**Dteyn's ATF projects**](https://github.com/Dteyn?tab=repositories&q=atf)

Aside from sharing [my coding projects on GitHub](https://github.com/Dteyn), I also enjoy streaming on Twitch. I usually stream weekly, feel free to pop by the stream some time!

https://twitch.tv/Dteyn

I also have a YouTube channel where I post various videos, especially After the Fall content. Check it out!

https://youtube.com/@Dteyn

Finally, if you found this project useful and feel like sending a few bucks my way, I also have a Ko-Fi page here:

https://ko-fi.com/Dteyn

Make it a great day! :)

You are visitor: ![Page views](https://dteyn-rad-page.netlify.app/.netlify/functions/pageviews?repo=ATFMutationStation)

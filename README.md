# ATF MutationStation

<img width="691" height="200" alt="image" src="https://github.com/user-attachments/assets/dfd96ad9-e91b-4e7b-94d3-9b8eadf24c33" />

**ATF MutationStation** is a mod for creating custom Mutator Runs in [After the Fall VR](https://www.afterthefall-vr.com/) by Vertigo Games.

This mod enables playing **any mutator on any level at any time**, instead of being restricted to only the 'current' mutator.

Currently, only **PCVR** versions are supported (Steam and Oculus Rift). Meta Quest, Pico, and PSVR are not supported.

> [!IMPORTANT]
> This mod is currently in **Beta** status - testing and feedback is encouraged to help work out any bugs before stable release. If you run into any issues, please open an [Issue](https://github.com/Dteyn/ATFMutationStation/issues) or DM me on Discord so it can be fixed. See [Known Issues](#known-issues) for things to be aware of, and the [Beta Testing](#beta-testing) section for things that are needing testing.

---

## Disclaimer

> [!WARNING]
> Modding is done at your own risk!!

___After the Fall is a multiplayer game, and when modding multiplayer games there is always a risk of being banned.___

While I've not heard of anyone getting banned for modding After the Fall, be aware that you are modding the game at your own risk.

In general, game mods can also cause unexpected behavior or crashes. While I can't guarantee problem-free modding, I'm happy to help troubleshoot if you run into issues.

---

## Table of Contents

* [Disclaimer](#disclaimer)
* [What does ATF MutationStation do?](#what-does-atf-mutationstation-do)
* [Compatibility](#compatibility)
* [Installation](#installation)
* [Uninstallation](#uninstallation)
* [Using the GUI](#using-the-gui)
* [Advanced Usage (Editing CFG Directly)](#advanced-usage-editing-cfg-directly)
* [Known Issues](#known-issues)
* [Troubleshooting](#troubleshooting)
* [Feedback & Support](#feedback--support)
* [Shout-Outs](#shout-outs)

---

## What does ATF MutationStation do?

ATF MutationStation lets you customize Mutator Runs in *After the Fall VR* by allowing you to freely select your preferred level and mutator package.

Normally, the game restricts mutator packages and levels to a set combo, rotating every two hours. With this mod, you can choose **any level with any mutator at any time you wish**.

### How is it used?

The mod changes the mutator displayed on the Enlisting machine in the lobby. Once the mod is installed and you've selected a level and mutator package, loading into the game will show your selection on the Enlisting machine.

Hot reload is supported. The settings are reloaded when you load into The Line, so changing settings between runs is possible without restarting the game.

> [!NOTE]
> For playing a custom level on the current mutator, **only the host** needs the mod installed. If playing custom levels and custom mutators, ___all players___ need the mod installed.

### Mutator Packages

By default, ATF has five "Mutator Packages" which the game developers created. Each package has 3 individual "mutator effects" as noted below:

#### Speed Runner
* **Time Trial**: 15 Minutes to Complete the Run
* **Dry Season**: Health Can No Longer Be Restored
* **Sleight Of Hand**: Advanced Reload Only

#### Gun Slinger
* **Sleight Of Hand**: Advanced Reload Only
* **Ammo Shortage**: Max Ammo is Halved
* **Berserk**: Snowbreed Deal Double Damage

#### Snapping Turtle
* **Ice Plating**: Snowbreed Have 100% Armor
* **Low Profile**: Snowbreed Crawl Instead of Walk
* **Case Hardened**: Snowbreed Take No Explosive Damage

#### Crowd Control
* **Ice Plating**: Snowbreed Have 100% Armor
* **Infestation**: 50% Increase in Snowbreed Spawn Rate
* **Tough Skin**: Snowbreed Health is Doubled

#### Snow Plow
* **Motor Function**: Snowbreed can only be killed with Headshots
* **Evolution**: Snowbreed do not Mutilate or Stagger
* **Cold Feet**: Movement Speed is Halved

### Mutator Effects

Here is a list of the 13 individual mutator effects:

* **Sleight Of Hand**: Advanced Reload Only
* **Dry Season**: Health Can No Longer Be Restored
* **Time Trial**: 15 Minutes to Complete the Run
* **Ammo Shortage**: Max Ammo is Halved
* **Infestation**: 50% Increase in Snowbreed Spawn Rate
* **Tough Skin**: Snowbreed Health is Doubled
* **Berserk**: Snowbreed Deal Double Damage
* **Ice Plating**: Snowbreed Have 100% Armor
* **Case Hardened**: Snowbreed Take No Explosive Damage
* **Motor Function**: Snowbreed can only be killed w/ Headshots
* **Evolution**: Snowbreed do not Mutilate or Stagger
* **Cold Feet**: Movement Speed is Halved

(note: there are 2 other effects defined that unfortunately don't work; see [Broken Mutator Effects](#broken-mutator-effects) for more info)

### Custom Mutator Packages

> [!NOTE]
> Currently, 'Custom Mutators' mode is under development and has some bugs. It can be accessed only via editing .cfg directly and results may vary. See [Known Issues](#known-issues) for more details.

By combining any of the above effects, you can create your own custom mutator packages. Choose the ones you want and let the chaos ensue!

---

## Compatibility

* Compatible with **After the Fall** version **1.9.41947** (aka "Nightfall Update").
* Tested and working on **PCVR** (both Steam and Oculus Rift versions).
* **Not compatible** with Meta Quest, Pico, or PSVR versions. Sorry!

Note that to play the *currently active mutator* on *any* level, **only the host** needs the mod installed. Unmodded players can join custom levels as long as you don't change the mutator selection.

However if selecting a custom mutator as well, **all players** must have the mod installed.

---

## Installation

1. **Download and Install**

   *  Grab the latest `ATFMutationStation-vX.X.X.zip` from the [Releases](https://github.com/Dteyn/ATFMutationStation/releases) section.
   
   * Extract the .zip file to your After the Fall game folder:

     * **Steam default location:** `C:\Program Files (x86)\Steam\steamapps\common\After The Fall`

     * **Rift default location:** `C:\Program Files\Oculus\Software\Software\vertigo-games-snowbreed`  

   To verify installation, check for the folllowing files in your game folder:

   * `BepInEx\plugins\ATFMutationStation.dll`
   * `BepInEx\config\com.dteyn.atf.mutationstation.cfg`

2. **Adjust Mutator Settings:**

   With the mod installed, you can now adjust mutator settings. You can do this in two ways:

   1. **Use the GUI to change settings** - see [Using the GUI](#using-the-gui)

   2. **Edit the config file manually** - see [Advanced Usage](#advanced-usage-editing-cfg-directly)

   The mod supports hot reload. When loading into The Line the config is reloaded, which allows you to change mutators between runs without restarting the game.

3. **Launch the Game:**

   Once you've changed the mutator settings, launch the game and your new mutator selection should be active on the Enlisting machine in the lobby.

> [!NOTE]
> On your first launch after installation, expect a slightly longer startup as BepInEx does some initial setup.

> [!IMPORTANT]
> This mod uses [BepInEx](https://github.com/BepInEx) version [___6.0.0-pre.1___](https://github.com/BepInEx/BepInEx/releases/download/v6.0.0-pre.1/BepInEx_UnityIL2CPP_x64_6.0.0-pre.1.zip). Other versions of BepInEx are not compatible. If you have an [OWO Vest](https://owogame.com), be aware that mod uses BIE 6.0.0-pre2 which is not compatible. I've recompiled the OWO mod for pre1 which can be obtained here: [OWO AfterTheFall v1.0.1 for BIE 6.0.0-pre1](https://github.com/Dteyn/OWO_AfterTheFall/releases/tag/1.0.1)

> [!TIP]
> The version of BepInEx used supports **Astienth's** **bHaptics** and **ProVolver** mods for After the Fall! Don't miss those if you have [bHaptics](https://www.bhaptics.com) or [ProVolver](https://protubevr.com) gear!

* [bHaptics mod for After the Fall](https://github.com/Astienth/AftertheFall_bHaptics)
* [ProVolver mod for After the Fall](https://github.com/Astienth/AfterTheFall_Provolver)

---

## Uninstallation

Disabling or removing ATF MutationStation is easy; you can use any of these methods:

* **Set selections to 'None'**: You can disable MutationStation by setting the level and mutator package to 'None' - doing this effectively returns After the Fall to it's stock behaviour, so you don't need to remove the mod to disable it. Just set both options to 'None' in the GUI or .cfg file.

or

* **Disable Mod Only:** Delete `ATFMutationStation.dll` from `BepInEx/plugins`. This will remove the .dll the mod uses, but will leave other mods intact. You can also create a new folder, `BepInEx/plugins-disabled` and move any plugins you wish to disable into that folder, then move back later to re-enable them.

or

* **Disable BepInEx Entirely (All Mods):** Rename `winhttp.dll` in the After the Fall folder to something different, like `winhttp-disabled.dll`. This will disable BepInEx entirely which disables all mods/plugins.

or

* **Complete Removal (Return to Vanilla):** Delete `BepInEx` folder, `mono` folder, and the files `doorstop_config.ini`, `winhttp.dll`, and `changelog.txt` from your game folder. You are now back to stock ATF with no mods installed.

---

## Using the GUI

<img width="691" height="200" alt="image" src="https://github.com/user-attachments/assets/dfd96ad9-e91b-4e7b-94d3-9b8eadf24c33" />

The MutationStation mod itself is controlled by a config file. To make life easier I've created a simple GUI which can be used to edit the config file and change mutator runs.

___NOTE: The GUI must be downloaded separately___; it's not included with the base mod. See instructions below.

### Versions Available

The GUI is available as a Python script, as well an `.exe` version. The only difference is the `.exe` version doesn't need Python installed since everything is self-contained in the `.exe`.

> [!NOTE]
> The `.exe` version is created using [PyInstaller](https://pyinstaller.org/); this method can sometimes trigger a virus warning.

Any virus warning can safely be ignored, but if it bothers you, using the Python script is recommended since you can easily inspect the source code if you wish.

Regardless of which version you choose, the recommended location is to place it within your `After the Fall` game folder, and then make a shortcut to it on your Desktop or Start Menu.

#### Standalone `.exe` version

1. Download `ATFMutationStation-GUI-exe-vX.X.X.zip` from the Releases section and extract it to your After the Fall game folder.

2. Run `ATFMutationStation-vX.X.X.exe` to start the GUI.

#### Python script version

1. Install Python 3.x (https://python.org)

2. Download `ATFMutationStation-GUI-Python-vX.X.X.zip` from the Releases section and extract it to your After the Fall game folder.

3. Run `ATFMutationStation-vX.X.X.pyw` to start the GUI.

#### GUI Usage:

> [!NOTE]
> Make sure you've installed the mod itself first per instructions above before running the GUI! The mod and GUI are installed separately.

> [!IMPORTANT]
> All players must be using the same version of the mod and using the same settings if playing with custom mutators. Otherwise, desynchronizations may happen resulting in invisible enemies or other strange issues.

Upon launching the GUI, you'll see a window with a box to select your After the Fall Game folder, as well as dropdown boxes to select mutators.

The GUI will expect the ATF MutationStation config file to be present at: `BepInEx\config\com.dteyn.atf.mutationstation.cfg`

* Select your After the Fall game folder which contains `AfterTheFall.exe`:
     * **Steam default location:** `C:\Program Files (x86)\Steam\steamapps\common\After The Fall`

     * **Rift default location:** `C:\Program Files\Oculus\Software\Software\vertigo-games-snowbreed` 

* Choose your level and mutator package from dropdown menus. You can choose from any of the pre-defined mutator packages.
* Click the Save Config button, then launch the game.

Your custom mutator selection should now appear in the Enlisting machine in The Line.


* ~~To create a custom mutator package, select "Custom Mutator Package" and pick any three mutators you wish.~~

> [!NOTE]
> The Custom Mutators feature is currently buggy and therefore only accessible from the .cfg file directly; it will be enabled in the GUI a future release.

> [!TIP]
> You can also change mutators while the game is running. The best time to do this is during a level, since when you load back to The Line the config is reloaded. You can also change it while at The Line, but you'll need to go into a level, then exit out to see the changes take effect.

---

## Advanced Usage (Editing CFG Directly)

The GUI is not required to use the mod; if you prefer a quicker approach you can simply edit the config file with a text editor to change mutator settings. The config contains documentation within.

### Location:

Once the mod is installed, the config file is located at: `\BepInEx\config\com.dteyn.atf.mutationstation.cfg`

### Config file example:

```ini
[General]
## Option: CustomGameplayLevel
## ===========================
## Description: Set the desired level for a mutator run.
## Options:
## - Skidrow
## - Chinatown02 (Chinatown)
## - Downtown (Quarantine Center)
## - BankTower (Union Tower)
## - BankTower02 (Relay Tower)
## - Boulevard
## - Bonaventura (Downtown)
## - Subway
## - Hospital
## Default: None
# Setting type: String
# Default value: None
CustomGameplayLevel = BankTower02

## Option: MutatorPackageId
## ==============================
## Description: Set the ID of the mutator package to force. Use -1 to disable.
## Options:
## - 0 = SpeedRunner - Mutators: 4,3,0
## - 2 = GunSlinger - Mutators: 0,5,8
## - 6 = SnappingTurtle - Mutators: 9,10,11
## - 7 = CrowdControl - Mutators: 9,6,7
## - 8 = SnowPlow - 12,13,14
## - 999 = Use Custom Mutators as defined in CustomMutators option
## 
# Setting type: Int32
# Default value: -1 (Disabled)
MutatorPackageId = 7

## Option: CustomMutators
## ======================
## Description: Comma-separated list of mutator IDs. Leave blank to disable custom mutator mode.
## Example: 0,3,9
## Options:
## - 0 = Sleight Of Hand: Advanced Reload Only
## - 3 = Dry Season: Health Can No Longer Be Restored
## - 4 = Time Trial: 15 Minutes to Complete the Run
## - 5 = Ammo Shortage: Max Ammo is Halved
## - 6 = Infestation: 50% Increase in Snowbreed Spawn Rate
## - 7 = Tough Skin: Snowbreed Health is Doubled
## - 8 = Berserk: Snowbreed Deal Double Damage
## - 9 = Ice Plating: Snowbreed Have 100% Armor
## - 10 = Low Profile: Snowbreed Crawl Instead of Walk
## - 11 = Case Hardened: Snowbreed Take No Explosive Damage
## - 12 = Motor Function: Snowbreed can only be killed w/ Headshots
## - 13 = Evolution: Snowbreed do not Mutilate or Stagger
## - 14 = Cold Feet: Movement Speed is Halved
## Default: none
## 
# Setting type: String
# Default value: 0,3,9
CustomMutators = none
```

| Setting                 | Description                                              | Example Values                                        |
| ----------------------- | -------------------------------------------------------- | ----------------------------------------------------- |
| **CustomGameplayLevel** | Selects level for the mutator run                       | Skidrow, Chinatown02, Downtown, etc. <br>None = default mutator level                  |
| **MutatorPackageId**    | Selects predefined mutator package | 0-14 or -1 = disabled <br> 999 = custom mutators                                |
| **CustomMutators**      | Mutator IDs to apply                | `0,3,9` (comma-separated mutator IDs) |

> [!NOTE]
> The CustomMutators option currently has some bugs - see [Known Issues](#known-issues) for details.

> [!IMPORTANT]
> All players must be using the same version of the mod and using the same settings if playing with custom mutators. Otherwise, desynchronizations may happen resulting in invisible enemies or other strange issues.

## Broken Mutator Effects

> [!WARNING]
> Mutator Effect IDs 1 and 2 are NOT working unfortunately.

A total of 15 effect IDs (`0` through `14`) are defined in the game data; however IDs `1` and `2` are not functional, as they seemingly never got implemented by the developers in the game code itself.

These effects are defined in the game data as:

```
Mutator Effect ID 1 = Intertwine: Shared Health Pool of 200
Mutator Effect ID 2 = Out Of Battery: Lose 1 Health On Missed Shot
```

From testing, trying to use these will result in the game refusing to process any other mutators in the list.

It may be possible to restore these mutator effects with further mods in the future that implement the intended functionality.

## Tips

* Hot-reload is supported; after saving, reloading into the lobby will reload the config file with updated mutator details. A game restart is not required.

* If you remove the .cfg file, a new one will be generated by the .dll when the game starts. The GUI will also generate a new .cfg if one doesn't exist.

---

## Known Issues

### [Custom Mutators not working as expected](https://github.com/Dteyn/ATFMutationStation/issues/1)

In release v0.3.0, the 'Custom Mutators' mode is not working as expected. Some mutators seem to work fine, but other mutators don't work (for example, 'Dry Season' still allows health restore).

In addition, it seems like residual mutator effects from the 'current' mutator are still active. I'll fix this in a future release but for now wanted to make v0.3.0 available as it works fine for selecting a custom level and predefined mutator package.

### [Mutator Title doesn't update in custom mutator mode](https://github.com/Dteyn/ATFMutationStation/issues/2)

When using a Custom Mutator Package, the name of of the mutator package is not updated which may be confusing.

In other words, if the current mutator is Snow Plow, it'll still say 'Snow Plow' on the enlisting machine, and in the game menu during the level - however the custom mutator effects you've chosen will be displayed properly. Only the title will be displayed incorrectly.

In a future version I intend to patch the mutator package title so it shows '**CUSTOM MUTATOR**' so this won't be confusing.

### [Mutator Title doesn't update when receiving an invite](https://github.com/Dteyn/ATFMutationStation/issues/3)

When an invite is received, it will display the current mutator regardless of which package may be selected. A fix will be required to update the popup notification to display the custom mutator selected (or 'CUSTOM MUTATOR' as described above).

---

## Troubleshooting

> [!IMPORTANT]
> All players must be using the same version of the mod and using the same settings if playing with custom mutators. Otherwise, desynchronizations may happen resulting in invisible enemies or other strange issues.

If something goes wrong, check these logs for signs of troubles:

* **BepInEx log:** `BepInEx\LogOutput.log` (within game folder)

* **ATF's Player.log:** `%LocalAppData%\Vertigo Games\AfterTheFall\Player.log`

For live logging, you can also edit `BepInEx\config\BepInEx.cfg` find `[Logging.Console]` and set `Enabled=true` which enables the BepInEx console.

* **ATF MutationStation GUI log** `output.log`

If using the GUI, you can also check the `output.log` file (in the same folder as the GUI `.pyw`/`.exe`)to see if it gives any hints of troubles.

---

## Beta Testing

As noted in [Known Issues](#known-issues), the Custom Mutators mode is still buggy and needs more testing. But before then, I need to fix the custom mutator mode, so testing in this area is currently futile until bugs are fixed.

With that said; anyone is still welcome to try out the custom mutator mode. It may not give expected results, but also won't break anything so there isn't a risk of harm or anything like that. It just may not have consistent results from my testing.

Below is a list of other things I can think of that need testing:

* Once fixed, all combinations of custom mutators need testing, none should crash the game or cause issues but it's possible there is some strange underlying issue

* I think it's possible to use more than 3 mutators at once. Editing the config manually should allow this, if this is working then I'll update the GUI so more than 3 can be selected.

* UX (User-Experience) improvements; if you run into anything confusing or something obvious that needs improving that I've missed, please let me know!

---

## Future Improvements

It would be useful to note which mutators require all players to have the mod installed, and which can be used as "host-only" mutators.

For example: 'Infestation' affects spawn rate which is on the host side, if only the host has 'Infestation' it will still work for the other players due to how the server/client architecture works.

However, local effects like 'Ammo Shortage' only affect on the client side, and will not transfer over so will not affect other players. This is not a major issue since this cannot cause a desync; other players simply will have their regular ammo ammount.

The real issue is with stuff like 'Case Hardened'; if one player has it enabled and the other doesn't, when explosives are used the snowbreed will die on one player's side but not the other player, and thus there will be invisible enemies due to the desynchronization.

This is why I'm currently recommending all players use the same settings; in the future this could be refined with more testing.

Other ideas:

- At the moment, the GUI is simple and fairly limited, I'd like to rewrite it in C# and have a nicer looking GUI to go alongside the app.

- An internal means to communicate the host's custom mutator selection to other players using the mod would be great, to prevent the need for each player to manually synchronize settings.

---

## Feedback & Support

Got issues, suggestions, or questions? Open an [Issue](https://github.com/Dteyn/ATFMutationStation/issues), or catch me on the [After the Fall Discord](https://discord.gg/afterthefall).

---

## Shout-Outs

### [Astienth](https://github.com/Astienth)

My good friend **Astienth** makes some amazing VR mods that you must check out!

He has made tons of **bHaptics** and **ProVolver** mods, including a [bHaptics mod for ATF](https://github.com/Astienth/AftertheFall_bHaptics) and a [ProVolver mod for ATF](https://github.com/Astienth/AfterTheFall_Provolver). Give them a try if you have haptic gear!

Astienth also makes a ton of other great flat2VR mods, be sure to check out his list of projects here: https://github.com/Astienth/VR-Mods-Projects

### [farmertrueVR](https://www.farmertrueVR.com)

My good friend **farmertrue** is a variety VR streamer who streams a wide range of VR content at the highest level possible.

He has a true passion for VR, and gives his honest opinion unlike so many other creators these days. He often streams the latest VR games, and if there is a bHaptics mod available, you can be certain he'll be using it.

Farmertrue also has a great 18+ Discord community, where we chat about VR on a daily basis, help users with PCVR builds or troubleshooting, and generally just chill out and have a great time hanging in VR. 

Be sure to check him out if you're looking for the best in VR entertainment and information!

- [www.farmertruevr.com](https://www.farmertrueVR.com)
- [twitch.tv/farmertrue](https://twitch.tv/farmertrue)
- [youtube.com/@farmertrueVR](https://youtube.com/@farmertrueVR)
- [Join the farmertrueVR Discord](https://discord.gg/SpKY7ySjXX)

### [Vertigo Games](https://www.vertigo-games.com/)

[After the Fall VR](https://www.afterthefall-vr.com/) was developed by [Vertigo Games](https://www.vertigo-games.com/), a Dutch game developer renowned for their expertise in creating high-quality virtual reality experiences.

In addition to *After the Fall VR*, they are also known for great titles like *The 7th Guest VR*, and the *Arizona Sunshine* series, both of which have received high accolades.

A big shout-out and heartfelt thanks to Vertigo Games for making After the Fall such an amazing experience that stands the test of time. The technical work put into the game engine is also an absolute marvel. I'm a huge fan of your work in every aspect!

<sub><i>PS: Please make an After the Fall 2! :)</i></sub>


## About Me

Aside from sharing my coding projects, I also enjoy streaming on Twitch. I usually stream GTFO VR Mod once a week, feel free to pop by the chat some time!

https://twitch.tv/Dteyn

I also have a YouTube channel where I post various videos, especially After the Fall content. Check it out!

https://youtube.com/@Dteyn

Finally, if you found this project useful and feel like sending a few bucks my way, I also have a Ko-Fi page here:

https://ko-fi.com/Dteyn

Make it a great day! :)

You are visitor: ![Page views](https://dteyn-rad-page.netlify.app/.netlify/functions/pageviews?repo=ATFMutationStation)

# Cryotherapy

- [Cryotherapy](#cryotherapy)
- [Preamble](#preamble)
- [Installation](#installation)
  - [Pre-Installation](#pre-installation)
    - [Installing Microsoft Visual C++ Redistributable Package](#installing-microsoft-visual-c-redistributable-package)
    - [Steam Config](#steam-config)
      - [Disable the Steam Overlay](#disable-the-steam-overlay)
    - [Change Steams Update Behavior](#change-steams-update-behavior)
    - [Set the Game language to English](#set-the-game-language-to-english)
    - [Clean Fallout 4](#clean-fallout-4)
  - [Using Wabbajack](#using-wabbajack)
    - [Preparations](#preparations)
      - [Problems with Wabbajack](#problems-with-wabbajack)
  - [Post-Installation](#post-installation)
    - [Copy Game Folder Files](#copy-game-folder-files)
- [Updating](#updating)
- [BiRaitBec Texture Optimization](#biraitbec-texture-optimization)
- [Noteworthy Mods](#noteworthy-mods)
  - [Frost Survival Simulator](#frost-survival-simulator)
  - [Fallout 2287 - Nuclear Winter](#fallout-2287---nuclear-winter)
  - [Fallout 2287 - Gas Masks of the Wasteland](#fallout-2287---gas-masks-of-the-wasteland)
  - [Agony](#agony)
  - [Better Locational Damage](#better-locational-damage)
- [Launching the Game](#launching-the-game)
- [In-Game MCM Options](#in-game-mcm-options)
- [FAQ](#faq)
- [Controller Support](#controller-support)
- [ENB](#enb)
- [Widescreen Support](#widescreen-support)
- [Credits and Thanks](#credits-and-thanks)
- [Contact](#contact)

---

# Preamble

### Cryotherapy

Cryotherapy is a relatively hardcore survival game based on [Frost Survival Simulator](https://www.nexusmods.com/fallout4/mods/18898). It is a dark, cold, dismal experience. I wish you the best of luck.

---

## Installation

### Pre-Installation

You need a legal copy of Fallout 4 through Steam, with all DLCs **EXCEPT** the High Definition DLC. This is garbage and should not be used in any case ever.

These steps are only needed if you install this Modlist for the first time. If you update the Modlist, jump straight to [Updating](#updating).

#### Installing Microsoft Visual C++ Redistributable Package

I doubt you need to do this since you likely already have this installed. The package is required for MO2 and you can download it from [Microsoft](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads). Download the x64 version under "Visual Studio 2015, 2017 and 2019". [Direct link](https://aka.ms/vs/16/release/vc_redist.x64.exe) if you can't find it.

#### Steam Config

##### Disable the Steam Overlay

The Steam Overlay can cause issues with ENB and is recommended to be turned off.

Open the Properties window (right click the game in your Library->Properties), navigate to the _General_ tab and un-tick the _Enable the Steam Overlay while in-game_ checkbox.

#### Change Steams Update Behavior

Fallout 4 is still being updated by Bethesda (they only add Creation Club content). Whenever the game updates, the entire modding community goes silent for the next one or two weeks because some mods need to be updated to the latest game runtime version.

To ensure that Steam does not automatically updates the game for you, head over to the Properties window, navigate to the _Updates_ tab and change _Automatic updates_ to _Only update this game when I launch it_. You should also disable the Steam Cloud while you're at it.

#### Set the Game language to English

Just do it. This entire Modlist is in English and 99% of all mods you will find are also in English. I highly recommend playing the game in English and **I will not give support to people with a non-English game**. I really wish I could, but at this time, it simply isn't feasible.

Open the Steam Properties window, navigate to the _Language_ tab and select _English_ from the dropdown menu.

#### Clean Fallout 4

I highly recommend uninstalling the game through Steam, deleting the game folder and reinstalling it. You should also clean up the `Fallout 4` folder in `Documents/My Games/`. **Make sure you run the game once** to establish your registry path - otherwise, Wabbajack will be unable to locate the game directory, and thus cannot install the modlist.

---

### Using Wabbajack

#### Preparations

Let's get to the actual installation..

Grab the latest release of Wabbajack from [here](https://www.wabbajack.org/#/). Click the big blue Download button. Place the `Wabbajack.exe` file in a blank folder at the root of a drive, such as `C:/Wabbajack`. Please do not put it in a Windows Protected Directory, such as Program Files or your Desktop.

Launch Wabbajack. When it is finished extracting and installing itself, select the `Browse Modlists` option. Click the Download arrow for Cryotherapy, and you will be forwarded to the next screen when it is finished.

Set the `Installation Location` to a blank folder at the root of a drive, such as `D:\Cryotherapy`. The `Download Location` will update automatically. Again, please avoid using Windows Protected Directories. To save space, use the same downloads folder you use for other Fallout 4 modlists. You may also delete the downloads AFTER Wabbajack turns green and says Installation Successful.

Click the `Play` arrow.

---

### Problems with Wabbajack

There are a lot of different scenarios where Wabbajack will produce an error. I recommend re-running Wabbajack before posting anything. Wabbajack will continue where it left off so you lose no progress.

**Could not download x**:

If a mod updated and the old files got deleted, it is impossible to download them. In this case just wait until I update the Modlist. I'm typically extremely quick to respond to a situation such as this.

Most commonly, this will happen if a mod is hidden from Nexus. Contact me in Discord if this happens, and I can force the list to show as Under Maintenance until it comes back, and then I can fix it when it's unhidden.

**x is not a whitelisted download**:

This can happen when I update the modlist. Check if a new update is available and wait if there is none.

**Wabbajack could not find my game folder**:

Wabbajack will not work with a pirated version of the game. If you own the game on Steam, go back to the [Pre-Installation](#pre-installation) step.

---

### Post-Installation

#### Copy Game Folder Files

After Wabbajack turns green and says Installation Complete, you can close it. Go to your installation folder (I will refer to this folder as the MO2 folder from now on) and you'll see a folder named `Game Folder Files`.

Copy the all of the files from the `MO2/Game Folder Files` directory into your game folder.

---

## Updating

If this Modlist receives an update, please check the Changelog before doing anything. Always backup your saves or start a new game after updating.

Cryotherapy updates based on a [Semantic Versioning](https://en.wikipedia.org/wiki/Software_versioning) system.

Generally speaking:  
- Full x.0 (2.0, 3.0, etc) updates requires a new game.  
- Major x.x (2.1, 2.2 etc) updates requires a new game.  
- Minor x.x.x (2.1.1, 2.1.2) updates can be applied to an ongoing playthrough.

**Wabbajack will delete all files that are not part of the Modlist when updating!**

This means that any additional mods you have installed on top of the Modlist will be deleted. Your downloads folder will not be touched!

If you wish for Wabbajack to ignore any additional mods you've installed, rename them to say `[NoDelete]` at the beginning of the name.

Updating is like installing. You only have to make sure that you select the same path and tick the _overwrite existing Modlist_ button.

---

## BiRaitBec Texture Optimization

**Yes this step is required, stop asking me every single day.**

 - *If you already have completed the BiRaitBec texture optimization process, you can just copy and paste those files into the folder for this modlist. It is identical.*

Go to [BiRaitBec’s Modding Guide](https://www.nexusmods.com/fallout4/mods/23556?tab=description).  
Manually download the **WorkBase** file.  
Manually download the **Main Repack** files (Part One, Part Two, and Part Three).  
  
Extract the WorkBase file with 7zip.  
You should have three folders inside of Workbase: OriginalBa2, PatchedBa2, and PatchedFiles.  
Navigate to your Fallout4/Data folder and **copy** these 15 files:  

'Fallout4 - Textures1.ba2'  
'Fallout4 - Textures2.ba2'  
'Fallout4 - Textures3.ba2'  
'Fallout4 - Textures4.ba2'  
'Fallout4 - Textures5.ba2'  
'Fallout4 - Textures6.ba2'  
'Fallout4 - Textures7.ba2'  
'Fallout4 - Textures8.ba2'  
'Fallout4 - Textures9.ba2'  
'DLCworkshop01 - Textures.ba2'  
'DLCworkshop02 - Textures.ba2'  
'DLCworkshop03 - Textures.ba2'  
'DLCRobot - Textures.ba2'  
'DLCCoast - Textures.ba2'  
'DLCNukaWorld - Textures.ba2'  

**Paste** these files into your **WorkBase/OriginalBa2** folder.
**Extract** Main Repack Part One into a new folder.
Inside the new folder, you should see another folder called “**textures**”. **Cut** this textures folder and **paste** it into **Workbase/PatchedFiles**.
**Repeat the previous two steps** for Part Two and Part Three of the Main Repack archives.
Run the **installer.bat** file inside of WorkBase.
When it is done, you'll see 15 new files inside of the `PatchedBA2s` folder. Cut or copy these archives. Navigate to your Cryotherapy mods folder and find the Workbase folder (`Cryotherapy/mods/[NoDelete] Workbase Optimized Textures`). Paste the archives into here.
  
After all of these steps are complete, you may delete the WorkBase folder. If you have the space, I advise making a backup of both the vanilla ba2 files as well as the patched ba2 files. It will save you the trouble of having to redownload them again later.

Your PatchedBA2 files should match these sizes:  
![alt text](https://i.imgur.com/62bn0ID.png)

---

## Noteworthy Mods

### [Frost Survival Simulator](https://www.nexusmods.com/fallout4/mods/18898)

Enter a frozen wasteland populated by people struggling to survive - and plagued by severe trust issues.

### [Fallout 2287 - Nuclear Winter](https://www.nexusmods.com/fallout4/mods/37988)

Expanding on the base survival mechanics, Nuclear Winter brings temperature and sickness into the limelight. Make sure to stay warm, or else...

### [Fallout 2287 - Gas Masks of the Wasteland](https://www.nexusmods.com/fallout4/mods/17491)

Nuclear winter hasn't only brought icy death - it also brings a whole lot of radiation. Wear your mask, keep a clear line of sight, and always carry extra filters.

### [Agony](https://www.nexusmods.com/fallout4/mods/25600)

Overhauls the vanilla healing system with more immersive bandages and medicinal needs.

### [Better Locational Damage](https://www.nexusmods.com/fallout4/mods/3815)

No more bullet sponges. Aim for the head if you can for quick kills, take out their legs to cripple their movement, break their arms to greatly reduce their offensive advantage. Think quickly, react accordingly.

---

## Launching the Game

After you copied the Game Folder Files, launch ModOrganizer.exe from inside your installation folder you chose for Wabbajack. Near the top of the left window in MO2, you will see this:  
![alt text](https://i.imgur.com/ifxpSO6.png)

Choose whatever faction you like. Other factions will be hostile or friendly depending on your decision. If you don't know what these factions are, don't worry about it. Choose one that sounds neat or simply choose No Faction.

Make sure the bar on the right side says `F4SE` and click Run. **You need to launch the game in this exact way every time in order to play with the installed mods.**

## In-Game MCM Options

 - *Note that hotkeys are personal preference. Don't set hotkeys to something that already has something else bound to it. For example, don't set Saving to F5 while Quicksaving is already set to F5.*
 
Baka Wait Anywhere.  
![alt text](https://i.imgur.com/4HV7RMS.png)

CCCleaner.  
![alt text](https://i.imgur.com/M8KDexv.png)  

FallUI Inventory. Optional. Personal preference, but I think Technical Blue suits the environment quite well. And it's just a nice color.  
![alt text](https://i.imgur.com/WYxT3h9.png)  

FallUI HUD. Make sure Lively's Frost HUD preset is selected.  
![alt text](https://i.imgur.com/PXHlwfw.png)  

Faster Workshop. Optional hotkey.  
![alt text](https://i.imgur.com/7cUugf9.png)  

Fallout 2287 - Nuclear Winter - Temperature Widget. Change the settings to match the ones seen in the image below, then click `[Set Temperature Widget]`.  
![alt text](https://i.imgur.com/MIqznHy.png)  

Fallout 2287 - Nuclear Winter - Insulation Widget. Set the hotkey of your choosing, then change the settings to match the ones seen in the image below. Then click `[Set Insulation Widget]`.  
![alt text](https://i.imgur.com/HXHCNVM.png)

LevelUpMenuEx. Optional hotkey for quick access to the perk chart.  
![alt text](https://i.imgur.com/xHVSnIU.png)

Survival Options - Save Options. Set a Hotkey for this. I use F9.  
![alt text](https://i.imgur.com/5O83SJ8.png)

DEF Mods -  Survival Stats Widget. Scroll to the bottom and click `Tune Widget Elements Position`.  
![alt text](https://i.imgur.com/2O19Jxv.png)

DEF Mods - Survival Stats Widget Positions. These should be set for you already. Press `R` to save their positions.  
![alt text](https://i.imgur.com/CmjBWDc.png)

---

You will receive some pop-ups shortly after starting. These explain many of the mechanics you'll be using. Please read them carefully.

For Fallout 2287, I recommend the `Medium Preset`:  
![alt text](https://i.imgur.com/O6RodVO.png)

For Nuclear Winter, I recommend the `Realistic Insulation` option:  
![alt text](https://i.imgur.com/9y1usWT.png)

The explanation about Temperature will pop up several times. You may choose to read them, take note of what's happening, or silence them. Your call.  
![alt text](https://i.imgur.com/keJ1nxd.png)

Soon, you'll be at the main starting room. Your HUD should look like this if everything was done correctly:  
![alt text](https://i.imgur.com/INa34se.png)

Open your Pipboy and navigate to your Misc Items. Open the NPCs Travel holotape. Set all DLC sections to a Preset of `[0]`. Then find the Synths entry and set that to `0` as well - these are outlined in the Holotape itself for your convenience.  

Each door is a different starting location. The "vanilla" Frost start is the far door on the right side. The rest is up to you.

---

## FAQ

As this list has not yet been officially released, there have been no questions asked.

---

## Controller Support

If you're playing with a controller (why?), your pipboy map won't work. Open the MO2 INI Editor, select fallout4prefs.ini, and scroll down until you see the `[Display]` section. At the bottom, you'll find two lines:  
`uPipboyTargetHeight=1400`  
`uPipboyTargetWidth=1752`  
Change these two lines to the following:  
`uPipboyTargetHeight=700`  
`uPipboyTargetWidth=876`  
Then find the `[General]` section and change `bGamepadEnable=` from a `0` to a `1`.

### ENB

I don't use an ENB. I never saw the need. The ENB binaries are present for other purposes. If you wish to add an ENB preset, go for it, but I will provide zero support for such endeavors.

## Widescreen Support

I don't own a widescreen monitor, so I can't help directly. I don't mind you guys helping each other though, obviously. A generous discord user by the name of bjdripley wrote an [Ultrawide Compatibility Guide](https://docs.google.com/document/d/1EbZ_DpyhctsrpBlylDYc2TXtm1NAOjkcYjRCNZsC958/edit) that you may find useful.

## Credits and Thanks

- Erri120, for all of your work on Wabbajack and the website, and for making a readme template like this easy for an idiot like me to use.
- AUGSpeed, for being a great source of information. I really look up to you, I respect the hell out of your work, and you're somehow the nicest damn dude on the planet.
- Kaethela, for all of your ongoing support - both in regards to the modlist and listening to my endless bitching.
- Total, for your multiple contributions and advice over the last year and a half (and counting).
- Last but *certainly* not least: Halgari, creator of Wabbajack, without whom none of us would be here. You have improved over 100,000 people's lives and never asked for a single thing in return. That's *insane*.

## Contact

I'm always available on the [Wabbajack Discord](https://discord.gg/wabbajack) and [my own personal Discord Server](https://discord.gg/yABEjwB).

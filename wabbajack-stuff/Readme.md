# Magnum Opus

- [Magnum Opus](#magnum-opus)
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
    - [Launching the Game](#launching-the-game)
- [Updating](#updating)
- [BiRaitBec Texture Optimization](#biraitbec-texture-optimization)
- [Noteworthy Mods](#noteworthy-mods)
  - [Sim Settlements 2](#sim-settlements-2)
  - [Subway Runner](#subway-runner)
  - [This is Trash - A Scrapping Alternative](#this-is-trash---a-scrapping-alternative)
  - [Buffout 4](#buffout-4)
- [Creation Club Support](#creation-club-support)
- [In-Game MCM Options](#in-game-mcm-options)
- [FAQ](#faq)
- [Controller Support](#controller-support)
- [ENB](#enb)
- [Widescreen Support](#widescreen-support)
- [Credits and Thanks](#credits-and-thanks)
- [Contact](#contact)

# Preamble

### Magnum Opus

Magnum Opus is what one would describe as a "kitchen sink list." There is no specific focus or aspect I really care about. There is no specific goal I'm trying to achieve. I just want to have fun.

This means if I like a mod, it's going in. There is no such thing as "it doesn't fit my aesthetic" or "it goes against the theme of the list." The theme is fun.

To that end, I like new content. I like new areas, new quests, new NPCs, new weapons, new outfits, new faces. You'll find all of that - and a whole lot more - in this list. I genuinely hope you enjoy it as much as I do.

This list is NOT built with Survival Mode in mind. I don't play it. I don't like it. If you want Survival, you should play [Fallout 4 Enhanced Edition](https://www.wabbajack.org/#/modlists/info?machineURL=fallout_4_enhanced_edition).

Is Magnum Opus for you? I don't know, but [this video by DroppedIceCream might help you decide](https://youtu.be/Q2s84pTpkwE).

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

### Using Wabbajack

#### Preparations

Let's get to the actual installation..

Grab the latest release of Wabbajack from [here](https://github.com/wabbajack-tools/wabbajack/releases). You need to download the `Wabbajack.exe` file ONLY. Place the `Wabbajack.exe` file in a blank folder at the root of a drive, such as `C:/Wabbajack`. Please do not put it in a Windows Protected Directory, such as Program Files or your Desktop.

Launch Wabbajack. When it is finished extracting and installing itself, select the `Browse Modlists` option. Click the Download arrow for Magnum Opus, and you will be forwarded to the next screen when it is finished.

Set the `Installation Location` to a blank folder at the root of a drive, such as `D:\Magnum Opus`. The `Download Location` will update automatically. Again, please avoid using Windows Protected Directories.

Click the `Play` arrow.

### Problems with Wabbajack

There are a lot of different scenarios where Wabbajack will produce an error. I recommend re-running Wabbajack before posting anything. Wabbajack will continue where it left off so you lose no progress.

**Could not download x**:

If a mod updated and the old files got deleted, it is impossible to download them. In this case just wait until I update the Modlist. I'm typically extremely quick to respond to a situation such as this.

Most commonly, this will happen if a mod is hidden from Nexus. Contact me in Discord if this happens, and I can force the list to show as Under Maintenance until it comes back, and then I can fix it when it's unhidden.

**Mega links aren't downloading**:

Download this manually, put the archive in your Downloads folder, and restart Wabbajack.  
 - [FO4LODGen Resources](https://mega.nz/file/BZhlVCAJ#s-GqqbnJlZDvCLPiRw1Wm1EWGqMQCuh4CR8Zzn8POM4)  

**x is not a whitelisted download**:

This can happen when I update the modlist. Check if a new update is available and wait if there is none.

**Wabbajack could not find my game folder**:

Wabbajack will not work with a pirated version of the game. If you own the game on Steam, go back to the [Pre-Installation](#pre-installation) step.

### Post-Installation

#### Copy Game Folder Files

After Wabbajack turns green and says Installation Complete, you can close it. Go to your installation folder (I will refer to this folder as the MO2 folder from now on) and you'll see a folder named `Game Folder Files`.

Copy the all of the files from the `MO2/Game Folder Files` directory into your game folder.

#### Launching the Game

After you copied the Game Folder Files, launch ModOrganizer.exe from inside your installation folder you chose for Wabbajack. Make sure the bar on the right side says `F4SE` and click Run. **You need to launch the game in this exact way every time in order to play with the installed mods.**

You may notice some mods are deactivated. These are for the Creation Club profile. Please see the [Creation Club Support](#creation-club-support) section a bit further down for more information.

## Updating

If this Modlist receives an update, please check the Changelog before doing anything. Always backup your saves or start a new game after updating.

Magnum Opus updates based on a [Semantic Versioning](https://en.wikipedia.org/wiki/Software_versioning) system.

Generally speaking:  
- Full x.0 (2.0, 3.0, etc) updates requires a new game.  
- Major x.x (2.1, 2.2 etc) updates requires a new game.  
- Minor x.x.x (2.1.1, 2.1.2) updates can be applied to an ongoing playthrough.

**Wabbajack will delete all files that are not part of the Modlist when updating!**

This means that any additional mods you have installed on top of the Modlist will be deleted. Your downloads folder will not be touched!

If you wish for Wabbajack to ignore any additional mods you've installed, rename them to say `[NoDelete]` at the beginning of the name.

Updating is like installing. You only have to make sure that you select the same path and tick the _overwrite existing Modlist_ button.

## BiRaitBec Texture Optimization

**Yes this step is required, stop asking me every single day.**

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
When it is done, you'll see 15 new files inside of the `PatchedBA2s` folder. Cut or copy these archives. Navigate to your Magnum Opus mods folder and find the Workbase folder (`Magnum Opus/mods/[NoDelete] Workbase Optimized Textures`). Paste the archives into here.
  
After all of these steps are complete, you may delete the WorkBase folder. If you have the space, I advise making a backup of both the vanilla ba2 files as well as the patched ba2 files. It will save you the trouble of having to redownload them again later.

Launch Mod Organizer 2, and activate the `[NoDelete] Workbase Optimized Textures` mod.

Your PatchedBA2 files should match these sizes:  
![alt text](https://raw.githubusercontent.com/LivelyDismay/Learn-To-Mod/main/images/workbase%20file%20sizes.png)

## Noteworthy Mods

### Sim Settlements 2

Rebuild the Commonwealth with a mysterious stranger in a brand new, fully voiced, and - quite frankly - absolutely amazing questline in this highly anticipated sequel-of-sorts to the original Sim Settlements. 

Read more about it [here](https://www.nexusmods.com/fallout4/mods/47976)!

### Creative Perks Plus

Perk overhaul built on top of another perk overhaul. Fancy!

Read more about it [here](https://www.nexusmods.com/fallout4/mods/49400)!

### Subway Runner

Explore an expansive, deadly metro system that stretches the length of the entire Commonwealth. No quests here, folks; only loot, exploration, death, radiation, and a new way to travel across the city.

Read more about it [here](https://www.nexusmods.com/fallout4/mods/18639)!

### This is Trash - A Scrapping Alternative

I got tired of individually scrapping every single leaf and rubbish pile every time I started a new game, so I took some inspiration from Wabbajack and automated it. Each settlement will now have a trash can next to the workbench. Scrap it and watch as the area is miraculously cleaned of all those stupid looking shrubs and garbage decals.

Read more about it [here](https://www.nexusmods.com/fallout4/mods/42552)!

### Buffout 4

The equivalent of SSE Engine Fixes, Buffout basically makes lists like this possible. Memory patches, achievements enabler, memory leak warnings, and so much more. This is likely the single most important mod in the entire list.

Read more about it [here](https://www.nexusmods.com/fallout4/mods/47359)!

## Creation Club Support

Magnum Opus now has support for some Creation Club mods as of version 3.2 of the modlist. To make use of this, you must follow a few steps:
1. Click the profile dropdown menu at the top left of Mod Organizer 2, and change the active profile to `Magnum Opus - CC Profile`.
2. Launch the game and download your CC mods from the in-game storefront.
  -  I recommend doing this after launching the game from Mod Organizer 2. This will make all the creations download into your `overwrite` folder, which will make the next step a bit easier.
3. Cut and paste all of your CC mods into `Magnum Opus\mods\Creation Club Content`. 
4. Activate the `Creation Club Content` mod in Mod Organizer 2.
  -  Please take note that you will need all of the CC mods I currently provide support for.

<details>
  
  <summary>Click this to expand the list of supported Creation Club mods</summary>
  
  * Anti-Material Rifle  
  * CR-74L Combat Rifle  
  * Arcade Workshop Pack  
  * Capital Wasteland Mercenaries  
  * Charlestown Condo  
  * Captain Cosmos  
  * Chinese Stealth Armor  
  * Doom BFG  
  * Doom Marine Armor  
  * Fantasy Hero Set  
  * Graphic T-Shirt Pack  
  * Gunners vs Minutemen  
  * Handmade Shotgun  
  * Heavy Incinerator  
  * Hellfire Power Armor  
  * Horse Power Armor  
  * Manwell Rifle Set  
  * Modular Military Backpack  
  * Morgan's Space Suit  
  * Neon Flats  
  * Noir Penthouse  
  * Nuka-Cola Collector Workshop  
  * Pint-Sized Slasher   
  * Prototype Gauss Rifle  
  * Quake Thunderbolt  
  * Sentinel Control System Companion  
  * Settlement Ambush Kit  
  * Shroud Manor  
  * Solar Cannon  
  * Tesla Cannon  
  * TransDOGrifier  
  * Tunnel Snakes Rule  
  * Virtual Workshop: Atomic Crater  
  * Virtual Workshop: Desert Island  
  * Virtual Workshop: GNR  
  * Virtual Workshop: Grid World  
  * X-02 Power Armor  
  * Zetan Arsenal  
  
</details>

Pipboy Paint Jobs and Power Armor Paint Jobs are **NOT** supported.

If you have a Missing Masters warning in Mod Organizer 2 after following this set of instructions for the Creation Club profile, then there are CC mods in this list you don't have.

If you have CC mods that aren't in this list, that means I don't own them (yet?), so I cannot provide support. I'm doing my best here, please bear with me.

You may also notice some other mods are deactivated in the CC Profile - namely, some armors, power armors, and weapons. This is because some CC mods act as pseudo variants of these, and I didn't want "doubles" essentially.

## In-Game MCM Options

*_Note: Anything involving hotkeys can be set up however you like. These are simply the way I have them set up for myself._

Baka Wait Anywhere  
![alt text](https://i.imgur.com/EGePAFk.png)

Companion Command Hotkeys  
![alt text](https://i.imgur.com/QMQqSSu.png)  

Custom Camera - Standard  
![alt text](https://i.imgur.com/UhgV6QN.png)  

Custom Camera - Power Armor  
![alt text](https://i.imgur.com/IwfxTSB.png)  

Custom Camera - Miscellaneous  
![alt text](https://i.imgur.com/ZTexP2Z.png)  

Custom Camera - Features  
![alt text](https://i.imgur.com/PuDef9C.png)  

DLC Timing - Automatron  
![alt text](https://i.imgur.com/gvWlkO6.png)

DLC Timing - Far Harbor  
![alt text](https://i.imgur.com/V8rJPdf.png)

DLC Timing - Nuka World  
![alt text](https://i.imgur.com/4zY7zCG.png)

DLC Timing - Vault-Tec Workshop  
![alt text](https://i.imgur.com/wVaClh8.png)

FallUI - Coloring  
![alt text](https://i.imgur.com/liVn6zL.png)

FallUI - Text Style  
![alt text](https://i.imgur.com/Z6e5BBg.png)

FallUI Workbench - Generic Settings  
![alt text](https://i.imgur.com/FfZ7WHC.png)

FallUI Workbench - Workbench List  
![alt text](https://i.imgur.com/hS3nr3Z.png)

Faster Workshop Hotkey  
![alt text](https://i.imgur.com/kkgYNFT.png)  

QuickTrade  
![alt text](https://i.imgur.com/KeyaCf5.png)

Sim Settlements 2 - Respect Build Limit - Off  
![alt text](https://i.imgur.com/nTuRz20.png)

Some people have reported Cinematic Mode does not allow city plans to build themselves. You may wish to disable that option as well.

Workshop Framework  
![alt text](https://i.imgur.com/QVjhlRd.png)  

Workshop Plus - Options - Disable Clear Weather.  
![alt text](https://i.imgur.com/BGZnDBG.png)  

Workshop Plus - Hotkeys  
![alt text](https://i.imgur.com/aklZPWs.png)

You and What Army - BOS  
![alt text](https://i.imgur.com/SMYUY4x.png)

You and What Army - Railroad  
![alt text](https://i.imgur.com/2CNBPVY.png)

You and What Army - Institute  
![alt text](https://i.imgur.com/fJquOpK.png)

**Holotape Settings:**   
Open the Beantown Interiors Holotape in your Pipboy and select the following options:  

  *  Customize Options  
  *  Other Options  
  *  Mod Compatibility  
  *  Enable Inside Jobs

True Storms Configuration Holotape  
![alt text](https://i.imgur.com/cOjL4z2.png)

That's it! Have fun!  

## FAQ

- Some of my perk chart icons are way off-center.

  - I know. I don't know how to fix it because I don't know how to use flash or jpexs. You can either accept this visual issue or you can...play something else. Sorry, I like the perks and the minor visual issues don't bother me.


- I am having random crashes.

  - Check Magnum Opus' Mod Organizer 2. Look at the top right corner for a red triangle with a yellow number. Click it. If one of the warnings says "incompatible plugins" and spits out an error about Buffout 4, then you're missing the memory patch. This can happen in some cases. Reinstall VCRedit, re-copy Game Folder Files, launch the game through MO2 once, and close it again. The warning should now be gone, Buffout should be loaded properly, and you can go on with your day.
  - Another common cause for this is faulty Workbase files. Go back and verify the sizes of yours match the image above. If not, redo the Workbase steps.


- Is Creation Club content compatible?

  - Some. Please see the [Creation Club Support](#creation-club-support) section above for details.


- Can I add more mods or remove some mods I don't want?

  - Can you? Yes. Will I help you? Maybe, but **please discuss it in either general channels or my personal Discord server**, and be sure to disclose the fact that you've edited the list before reporting any bugs or crashes. If you're open and honest with me, I'm honestly much more willing to help you through your issues.


- Why is my crosshair on my pipboy?

  - You can turn the Power Armor HUD Switcher holotape setting for [Hide Hud in Pipboy] to Off in order to hide the crosshair when not in power armor, but this also makes the pipboy look pretty terrible when using it inside power armor. Your call.


- Why can't I use multiple companions/why can't I use Dogmeat with a vanilla companion?

  - One follower is enough, and Heather (a modded follower from [here](https://www.nexusmods.com/fallout4/mods/23273)) doesn't occupy a "follower" slot, so you can have Heather + one other companion. Considering how overpowered that is, there is no reason I should add Dogmeat to the mix as well.


- I've been following along your [amazing and wonderful modding tutorials](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/Main.md) and they're great! But my added mods are breaking precombines/previs/making shit flicker in and out of existence a lot. What the hell, man?

  - Load your mods ABOVE all the `* Previs.esp` files in the load order.


- I've been following along your [totally shitty modding tutorials](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/Main.md) and they suck! My game keeps crashing when I add stuff after following your instructions! What the hell, man?

  - That sucks. Post in general-f4-discussions in the Wabbajack server, or any channel my personal discord server. If you're not a dick, I'm genuinely more than happy to help if I can.

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

I don't own a widescreen monitor, so I can't help directly. I don't mind you guys helping each other though, obviously. A generous discord user by the name of bjdripley wrote an [Ultrawide Compatibility Guide for Magnum Opus](https://docs.google.com/document/d/1EbZ_DpyhctsrpBlylDYc2TXtm1NAOjkcYjRCNZsC958/edit) that you may find useful.

## Credits and Thanks

- Erri120, for all of your work on Wabbajack and the website, and for making a readme template like this easy for an idiot like me to use.
- AUGSpeed, for being a great source of information. I really look up to you, I respect the hell out of your work, and you're somehow the nicest damn dude on the planet.
- Kaethela, for all of your ongoing support - both in regards to the modlist and listening to my endless bitching.
- Total, for your multiple contributions and advice over the last year and a half (and counting).
- Halgari, creator of Wabbajack, without whom none of us would be here. You have improved over 100,000 people's lives and never asked for a single thing in return. That's *insane*.

## Contact

I'm always available on the [Wabbajack Discord](https://discord.gg/wabbajack) and [my own personal Discord Server](https://discord.gg/yABEjwB).

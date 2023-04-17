## Post-Installation Instructions

---

#### Copy Game Folder Files

After Wabbajack turns green and says Installation Complete, you can close it. Go to your installation folder (I will refer to this folder as the MO2 folder from now on) and you'll see a folder named `Game Folder Files`.

Copy all of the files from the `MO2/Game Folder Files` directory into your game folder. To further clarify this, you are copying **the contents** of this folder, not the entire folder itself.

---

## BiRaitBec Texture Optimization

**YES, IT'S MANDATORY. STOP ASKING.**

This step hashes your vanilla files, just like Wabbajack hashes all the downloads and mods. They need to be PERFECTLY CLEAN AND UNALTERED (with the exception of the Game Folder Files in the previous step). If you'd like to be sure, just Verify Integrity of Game Files through Steam to make sure your Fallout 4 archives are pristine.

Go to [BiRaitBec Workbase Improved](https://www.nexusmods.com/fallout4/mods/57782) and download the Main File.  
Extract this archive into a blank folder, outside of a Windows protected directory (such as `D:/Workbase Improved`).  

Now go to [BiRaitBec’s Modding Guide](https://www.nexusmods.com/fallout4/mods/23556?tab=description).  
Manually download the **Main Repack** files (Part One, Part Two, and Part Three).  

Finally, go to [SavrenX HD 1K Buildings and Interior](https://www.nexusmods.com/fallout4/mods/40534?tab=files) and **ONLY** download the last Update File entitled `Fix Vault-Window-Metal-Institute`.

DO NOT UNPACK any of these archives. Simply **COPY** the archives into the `D:/Workbase Improved/Repack7z` folder.

Go back to your `Workbase Improved` folder. Double click the `Installer.cmd` file to run it.  
  - If the file opens up in Notepad instead of running, simply close it and instead right click on the file and choose `Open`.

Choose the output of your liking. You may use the default `PatchedBa2` folder, or navigate to your Magnum Opus installation and select `mods/[NoDelete] Workbase Optimized Textures`.  
PowerShell will now launch and begin verifying all of your archives, then repacking your .ba2 files.  
**This process may take an hour or two, depending on your hardware. For most people, it takes about fifteen minutes.**  
When the installer is finished, it will automatically close itself.
  -  If you chose the default `PatchedBa2` folder for your output, navigate to that folder, select all the archives inside, Copy them (right click > copy, or Ctrl+C). Then navigate to `Magnum Opus/mods/[NoDelete] Workbase Optimized Textures` and paste the archives here (right click > paste, or Ctrl+V).

Due to how Wabbajack works, you only need to do this step ONCE. The `[NoDelete]` flag will prevent Wabbajack from ever deleting this mod during updates, so you will never have to redo this step unless you delete it yourself. Huzzah!

*Many thanks to Rux616 for the Workbase Improved installer, please do go show him some love and endorse his work.*

---

#### Launching the Game

After you copied the Game Folder Files, launch ModOrganizer.exe from inside your installation folder you chose for Wabbajack. Make sure the bar on the right side says `F4SE` and click Run. **You need to launch the game in this exact way every time in order to play with the installed mods.**

You may notice some mods are deactivated. These are for the Creation Club profile. Please see the [Creation Club Support](#creation-club-support) section a bit further down for more information.

---

## Creation Club Support

**A note from Lively:** CC Support sucks. The profile can often crash for some users due to what's called an Archive Limit. This variable tends to change for people and we have no idea why. The Creation Club mods don't add that much and most of them aren't that good. **I do not recommend buying them.** Besides, there is allegedly a Fallout 4 update coming soon that will include all the CC content, so just wait for that.  

Magnum Opus now has support for some Creation Club mods as of version 3.2 of the modlist. To make use of this, you must follow a few steps:
1. Click the profile dropdown menu at the top left of Mod Organizer 2, and make sure the active profile is set to `Default`. If the default profile doesn't exist, just launch it through Steam.
2. Launch the game and download your CC mods from the in-game storefront.
  -  Launching the game from Mod Organizer 2 will make all the creations download into your `overwrite` folder, which will make the next step a bit easier.
  -  If you had to launch it from Steam, then all of these CC modules will be in your `steamapps/common/Fallout4/Data` folder.
3. Cut and paste all of your CC mods into `Magnum Opus\mods\Creation Club Content`. 
4. Activate the `Creation Club Content` mod in Mod Organizer 2, then change the active profile to `Magnum Opus - CC Edition`.
  -  Please take note that **you will need all of the CC mods listed below** in order for the CC Edition profile to work, and **only** these CC mods. No more, no less. The list of required Creations is below:  

<details>
  
  <summary>Click this to expand the list of supported Creation Club mods</summary>
  
  * Anti-Material Rifle  
  * Arcade Workshop Pack  
  * Capital Wasteland Mercenaries  
  * Captain Cosmos  
  * Charlestown Condo  
  * Chinese Stealth Armor  
  * CR-74L Combat Rifle  
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

**Again, this profile will be used at your own risk.**

---

## A Few Quick Notes

 - It is recommended that you leave Vault 111 prior to reporting any issues to me. Please.
 - Your Pipboy flashlight will not work between the time you pick it up and the time you press the button to open the vault door. It genuinely amazes me how many people report this to me. Just press the button, it's right there.
 - You will get a few pop-ups upon exiting Vault 111. For ECO, select this option:  
![alt text](https://i.imgur.com/2F0OnWN.png)

---

## In-Game MCM Options

After leaving Vault 111, pop open your MCM Config and follow these instructions.  
*_Note: Anything involving hotkeys can be set up however you like. These are simply the way I have them set up for myself._

**MCM Settings Manager**  
Apply the `Magnum Opus MCM Settings` Preset.  
![alt text](https://i.imgur.com/WPIBXJ3.png)

**ECO - Legendary Injector**  
![alt text](https://i.imgur.com/KU1eTeB.png)

True Storms Configuration Holotape  
![alt text](https://i.imgur.com/cOjL4z2.png)

That's it! Have fun!  

---

## Contact

I'm always available on the [Wabbajack Discord](https://discord.gg/wabbajack) and [my own personal Discord Server](https://discord.gg/yABEjwB).


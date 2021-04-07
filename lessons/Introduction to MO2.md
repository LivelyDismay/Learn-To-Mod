# Introduction to Mod Organizer 2

In order to effectively modify a game, you need a way to manage all the files you are adding. There are a few different mod organizers out there. MO2 and Vortex are really the only two modern ones worth considering. We are only going to talk about MO2 since that is what you are using. 

So you want to add a mod to your vanilla game. Well first, what is a mod? All that a mod is, is a collection of files that alter the vanilla game. That’s it. Mods can contain different kinds of files, also called assets. The game will only load these files if they are in the Data folder of the game, and you can only have one version of each file in a given folder. Oh no! That’s a problem if you start adding multiple mods with the same file names. Maybe you want part of one mod, but a different part of another (such as the HUD in Magnum Opus which combines something like 11 different mods).

This is where MO2 shines. MO2 uses a Virtual File System to manage all these different mods. Each mod is stored in its own folder which is located in MO2\mods.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro1.png)  

These mods are displayed in the left pane of MO2.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro2.png)  

If you load FO4 through MO2 using F4SE, when the game looks for a file in the Data folder, MO2 re-directs the game to the folder that contains the needed file. Pretty neat. Now you can add a mod without contaminating the Data folder. That makes it easy to add or remove mods (Please don’t remove mods mid save. You WILL break your save irreparably).

Ok, too much talk, more pictures. This is what you see when you open MO2. First off, let’s close the log at the bottom. It takes up valuable real estate and doesn’t provide much day to day information. Click the X to close it. If you want to see it again, in the toolbar click, View, Log.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro3.png)  

You can see all of the mods that go into making Magnum Opus in the Left Pane. They have been put in the correct order by Lively, and are grouped by Separators. You can expand or collapse them to see what is inside. For now, let’s right click on a separator in the left pane, and choose Expand All. Now you can see all the mods in Magnum Opus.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro4.png)  

In the heading bar, you can see the column labeled Priority. Make sure you are sorting by that column, with 1 at the top, and the highest number at the bottom. The order of these mods is critical. The game loads mods from the top to the bottom. Let’s say you have two mods that change the appearance of a weapon. Only the files that get loaded last (at the bottom) make it into the game. Here’s an example.

In the filter below the left pane, type “Shotgun”. Double Click on “Stevens M-520 Shotgun” to open the mod. If you click on Filetree, you can see every file in the mod.    
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro5.png)  

This mod has materials (information about how textures, or appearance, map to meshes), meshes (the shape of the actual object), sound, and texture files. There is a plugin (esp) that contains data used by the game. The Meta.ini just contains information about the mod from Nexus; it has no impact on your game. 

Now click on Conflicts, and then on the Advanced tab.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro6.png)  

You can see this mod has many files that are only provided by this mod. But it also has a file that overwrites PL-14 Lebedev. So the version of PersistantSubgraphInfoAndOffsetData.txt from PL-14 Lebedev won’t ever be seen in game. The version from this mod though is also overwritten by multiple other mods, so this version won’t be in game either. You can see some .hkx (animation files) are overwritten by BCR – StevensM520. So the game will use those reload animations, but otherwise will use the animations from this mod. Things can get complicated quickly. MO2 has functions to quickly allow you to choose which version of a file you want, but instead of getting into those weeds now, we’ll move on.

Ok, close this mod, and scroll down to view it in the left pane (priority 308). Single click it in the left pane. Now it is highlighted in green, and you can see there are different mods highlighted in green and red. This quickly shows you which mods are being overwritten by Stevens M-520 or are overwriting it. You can also see this symbol that tells you this mod adds files and has files being overwritten.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro7.png)  

Browse through the other columns, see what information they provide. You can customize the left pane by right clicking the header bar as well. Right click the header bar, and enable Content.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro8.png)  

Now if you hover over the content column in the Stevens M-520 Shotgun row, you can quickly see what is inside that mod.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro9.png)  

You can change the priority of a mod by dragging and dropping it in the left pane, but do not do that now. 

Now let’s look at the right pane.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro10.png)  

This pane shows all of the plugins contained inside the mods. Plugins contain the actual information that makes the game. Just like the left pane, the order is critical, as the game loads from top to bottom. If two plugins alter the same record, only the record that loads last will make it into the game. xEdit and the CK are the main tools we use to view and edit the information in these files. The treasure chest means that the plugin will load a .ba2 file, or archive. Think of it as a zip file of assets used by the game. The yellow dot means that the plugin is flagged to load in ESL-space.

In the upper right section, you see the executable bar.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro11.png)  

Any program that is run from here will use the virtual file structure generated by MO2. If you load Fallout 4 using the Fallout 4 Script Extender (F4SE) you should see your modded game. If you load Fallout 4 through Steam though, you will only get a vanilla experience, because your mods don’t actually live in the Data folder. You can add new programs by clicking the Gears button above the left pane.

Let’s quickly talk about profiles. Above the left pane, you can see the name Magnum Opus.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro12.png)  

This is your main Magnus Opus profile. If you start adding stuff, don’t do it on this profile! Consider this your stable base that you know works and can always revert back to. Let’s make a new profile. Click the profile bar and scroll to the top. Click Manage Profiles. Alternatively, click the ID card button that says Manage Profiles. Highlight Magnum Opus and click Copy. Rename it something like – Modded Magnum Opus. Make sure both boxes are checked.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro13.png)  

Highlight the profile and choose Select. Now when you add mods and activate them, or rearrange them on this profile, your stable base will remain unchanged. Before we stop, let’s switch back to the main Magnum Opus profile. Then right click on any separator in the left pane, and choose, Collapse All.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/2ed192a11d4b167e260a5616161418297fe13b7e/images/mo2intro14.png)  

I hope you can start to see the power of file management using MO2.

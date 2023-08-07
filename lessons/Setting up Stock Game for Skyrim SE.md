# Setting up Stock Game for Skyrim SE - by Althro

## Summary
This guide will show you how to set up stock game, setup Mod Organizer 2 for Stock Game, get the paths correct for tools such as xEdit. The guide will use Skyrim Anniversary Edition for the setup; however, the same process applies to regular Skyrim Special Edition. This guide assumes you have all the tools such as Creation Kit, Mod Organizer, xEdit and others already downloaded.

## Introduction
You may have seen some Wabbajack modlist use a new feature called "Stock Game" or "Game Root" and wondered what that is or how to use it yourself. Stock Game is where you effectively make a copy of the game you wish to run in a new folder and redirect the paths so that when you launch a modlist, it launches that version of the game. It is especially useful if you wish to have multiple modlists as it means you keep your base Skyrim folder clean.

## Initial Setup
### Installing Skyrim
The first step in the procedure of setting stock game is ensuring that you have a completely clean and fresh installation of Skyrim. This must not be modified in any way, save for downloading the CC content. We won't cover how to reinstall the game, but it is relatively simple. Make sure you are installing it somewhere outside of Program Files.

Once you have redownloaded the game, run it once to have it download all the CC content. This may take a while depending on your internet speed and might fail a few times. Simply go into the Creation Club section and press the "download all" button.

### Making the Game Root and Copying across the files
To make the Stock Game folder, complete the following.

1. Make a new folder in a location that is on the root of your drive, or in a location such as `C:\Games\`
2. Make another new folder inside of that called "Game Root" or "Stock Game" (I prefer Game root).
3. Open that folder and then open a new explorer window.
4. Navigate to where your Skyrim is installed. It is typically nested similar to `\steam\steamapps\common\Skyrim Special Edition`.
5. Select everything in the folder **EXCEPT `gpu.txt`** and **copy** it into the folder you just created. **DO NOT MOVE IT.**

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%201.png)

*Everything that is not gpu.txt*

### Setting up Mod Organizer 2 to use the Stock Game
*Note: This section is designed for use with the Archive version of Mod Organizer 2. I do not use the installer version, only the archive version*

Open the MO2 archive and copy across all the data inside the zipped file to the master folder which you initially created. **Do not copy it to the game root folder.** Your folder should look like this picture.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%203.png)

Double click the ModOrganizer.exe file to open Mod Organizer. Create a new Portable instance and map the game location to be the `Game Root` folder which has your Skyrim install in. **Ensure this is correct by pressing the back arrow to ensure it is mapped correctly. It should look like the picture below**.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%204.png)

Finish setting up the Instance. 

### Cleaning up the CC content
Upon opening MO2, if you are using Anniversary Edition, you will be greeted by the sight of many unmanaged mods. To clean this up complete the following.

1. Create a new mod called `Creation Club`
2. Right click on the mod and open it in explorer.
3. Open the `Stock Game` folder and go into the `Data` folder.
4. Select all the files that start with "cc" 
5. Move these files to the `Creation Club` folder
6. Once complete, your folders should look like the picture below.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%205.png)

7. Close both folders and press F5 to refresh Mod Organizer. Your Mod Organizer should look like the picture below.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%206.png)

## Tool Setup

### SKSE
SKSE is simple to setup. Instead of copying the exe and dll's to your base Skyrim install, simply copy them into your stock game folder. Install the scripts as a mod in MO2 and you are completed.

### Engine Fixes
Engine Fixes is like SKSE in that it is very easy to setup. As before, simply copy the part 2 files into your stock game folder.

### Creation Kit
The Creation Kit is similar in terms of ease of use. You will need the main file from [Tweaked Creation Kit Ini](https://www.nexusmods.com/skyrimspecialedition/mods/19817) and I highly recommend using [SSE Creation Kit Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/20061) & [SSE Creation Kit FonixData Lip Sync Fix](https://www.nexusmods.com/skyrimspecialedition/mods/40971) alongside the Creation Kit. To setup the Creation Kit, complete the following steps.

1. Copy the Creation Kit.exe, CreationKit.ini & CreationKitPrefs.ini to the game root folder.
2. Extract and copy the Tweaked ini into the game root folder.
3. Copy the files from Creation Kit Fixes into the game root folder. If you receive a prompt to overwrite files, **do not overwrite**.
4. Install the Lip Sync Fix mod as normal in MO2.
5. Run the CK to test and make sure that it works.

### xEdit & xEdit based applications (DynDOLOD, xLodGen)
xEdit and applications based off it require the addition of some arguments to ensure that they can see where the data folder is. The most important argument to add is this one `-D:"C:\Path\To\Folder\Game Root\Data"` replacing the "Path\To\Folder" with the location of your game root folder. It should similar to the picture below.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%207.png)

Once you have added those arguments and saved them, run xEdit to ensure that it can properly read the data folder. If you see a picture like this, xEdit is working.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%208.png)

### Nemesis
For Nemesis to work with Stock Game, you need to adjust one of the lines in the Nemesis ini. To do this, complete the following steps.

1. Open the Nemesis mod and go to the `Ini Files` tab.
2. Select `Nemesis.Ini`
3. In the `SkyrimDataDirectory` line, change `auto` to the location of your data directory.
4. Save the ini file.

The picture below shows how the ini file should look.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%209.png)

### Synthesis
Synthesis is relatively simple to configure for Stock Game. Like Nemesis, you just need to tell it where your game data folder is. To configure Synthesis, complete the following steps.

1. Run Synthesis and select the game you are using (in my case Skyrim Special Edition)
2. Click on the `Skyrim Special Edition` text in the top right corner.
3. In the `data folder location` field, add where your stock game is. It should look like the picture below.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%2010.png)

4. Synthesis will auto-save this data and remember it for future times you run it.

### zEdit
zEdit is again a relatively simple tool to configure for Stock Game. Like the previous two tools, you just need to tell it where your game data folder is. To configure zEdit, complete the following steps.

1. Run zEdit and select the tool you want. **Do not run any tool yet**
2. Press the settings cog to open the game profiles configuration.
3. Change the `Path` field to where your stock game is. It should look like the picture below.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%2011.png)

4. Run the application to ensure that it picks up your data folder.

### Easy NPC

EasyNPC does not require any special setup other than simply making sure the checkbox marked `Use mod directory setting from mod manager when available` is checked.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%2012.png)

### PCA SE

PCA SE does not require any special setup other than telling it where the game is.

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%2013.png)

### Wrye Bash

To setup Wrye Bash, an additional argument must be passed to the executable. This argument is `-o "C:\\Path\\To\\Folder\\Game Root\\"`, making sure to use double blackslashes, like so:

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/Stock%20Game%2014.png)

To make sure it works, you should launch Wrye Bash, and it should take you directly into its main screen. If Wrye Bash goes into a screen that asks you to choose a game to manage, you got the path wrong.

## Conclusion
Whilst Stock Game might seem like a difficult thing to setup, in actuality it's not that tricky. By ensuring you use the correct paths and tell tools where things are, you can have totally seperated instances of modded games.

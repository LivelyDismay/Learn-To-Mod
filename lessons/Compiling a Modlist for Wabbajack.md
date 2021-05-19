# Compiling a Modlist for Wabbajack

So you want to create a Wabbajack modlist installer, either to keep as a personal backup or to share with your friends, or heck, maybe even to get onto the Wabbajack UI? The process may seem intimidating at first, but I assure you, it's much easier than it seems. Here's how it's done.

## Disclaimers

* This guide assumes you're using Mod Organizer 2 and are compiling a modlist for a Bethesda game. Specifically, Skyrim Special Edition will be used for this example, as this is the most common use case for Wabbajack.
* This guide assumes you have working knowledge of Mod Organizer 2 and its various functions - the focus is on using Wabbajack to compile a modlist installer, not how to use MO2.
* This guide assumes that you are either about to begin building a modlist for compilation or have already completed one. Instructions on how to build a load order, install mods, etc. will not be included.
* Some of this information is repeated from [Wabbajack's readme](https://github.com/wabbajack-tools/wabbajack/blob/master/README.md), where you can find more detailed information about things like special flags.

## Mod Organizer 2 Preparation

Before you begin creating a modlist installer, there's some basic setup that needs to be done with Mod Organizer 2.

1. Your copy of Mod Organizer 2 needs to be a portable copy of the program. This is an option presented to you when you install and run MO2 for the first time.

![](https://i.imgur.com/9soWRrw.png)

2. Your copy of Mod Organizer 2 should be set to use a dark theme. This is both a courtesy to the people who will be installing your modlist and a way to know for certain that the installation completed properly quickly and easily.

![](https://i.imgur.com/rQ0fY28.png)

3. You should have a profile in MO2 which you will use for compilation. It is recommended to keep this separate from the Default profile. The name of the profile doesn't matter, but common practice is to name the profile you use to compile the same as your modlist (excluding any version number or additional identifiers).

![](https://i.imgur.com/iix8lTJ.png)

4. The files downloaded for the modlist you wish to compile should be kept separate from any other mod download folders you have. It doesn't particularly matter what folder, as long as the only files in that folder are the archives and .meta files for *only* the mods used in the modlist. This is to prevent Wabbajack from downloading *everything* inside that "shared" download folder. When a user installs your modlist, you only want them to download the mods required to build your modlist. Including a bunch of extra downloads that aren't used just extends the download/install time and wastes precious hard drive space.

5. Before you begin the compilation process, you should make sure that Mod Organizer 2 is closed. Additionally, do not make any changes to the files contained within the folder where your portable instance is located.

## Beginning the Compilation Process

Now that you've set up MO2 properly and have completed building your modlist, it's time to download and open Wabbajack.

1. Download Wabbajack from [its website](https://www.wabbajack.org/#/).
2. Place the Wabbajack.exe in its own folder, usually located at the root of your primary hard drive. Ex: C:\Wabbajack\Wabbajack.exe
3. Run Wabbajack.exe

You'll be presented with the following screen. We're interested in the "Create a Modlist" button.

![](https://i.imgur.com/xKLDNZQ.png)

When you click this button, you'll be presented with a whole lot of empty boxes. The very first thing you need to do is click the 3 dots next to the "Modlist Location" box.

![](https://i.imgur.com/8qTzMlw.png)

When you do, you'll be prompted to find a file. You're looking for the modlist.txt for the MO2 profile you want to turn into a Wabbajack installer.

![](https://i.imgur.com/VgdS15N.png)

When you have located it, open it. Wabbajack will auto-complete some information for you, namely (heh) the Modlist Name. Next, you need to fill out the Download Location. This is the *folder* that contains all of the downloads specific to your modlist. Remember earlier we kept those downloads separate from any other mod download folders. Click the three dots in the "Download Location" box.

![](https://i.imgur.com/g17cca6.png)

You'll again be prompted to find something, but this time, we're looking for a *folder* instead of an individual file. 

![](https://i.imgur.com/8pOoi2A.png)

Next, you'll want to fill out the "Output Location" field. Click the three dots next to that box.

![](https://i.imgur.com/WVJLnUa.png)

The path you now select is where your modlist installer file will be created when Wabbajack is finished. Make it somewhere easy to remember so you can easily find it when needed.

Now, the only other required field is the Version field. You can put any combination of numbers and dots (periods) you want. Common practice is to use x.y.z notation, where X is major list versions, Y is minor list versions, and Z is incremental list versions. How exactly you want to do your version numbering is entirely up to you.

![](https://i.imgur.com/o2KOaL1.png)

You *can* fill out the rest of the fields and *absolutely should* if your modlist is going to have any sort of public release. 

* Author - your username
* Description - a brief description of the modlist
* Image - an image that represents your modlist and is shown during installation
* Website - a link to your website
* Readme - a link to the readme for your modlist
* NSFW Checkbox - this should be checked if your modlist contains explicit NSFW content

With all of that filled out, you're now ready to click the Compile button!

![](https://i.imgur.com/qOHNaFX.png)

Wabbajack will now begin the process of compiling your modlist installer.

## Compilation

During the compilation process, you'll notice that Wabbajack is doing a lot of things. Each thing that Wabbajack does can take a variable amount of time based on how fast your PC's processor and internet are. In brief, these are the steps Wabbajack takes to build your modlist installer file:

1. Wabbajack will first check all of the files that are in your modlist's game's folder (basically, the vanilla game) to see if there are any it needs to use to build the modlist. It will also extract any archives that are new that it hasn't seen for this particular modlist before so it can check against those later if they are necessary to build the modlist. This is generally called "Indexing". Effectively, Wabbajack is figuring out what it has available to work with so that later on it knows what it can use to build the modlist installer file and also verify that what it has to work with matches what the modlist needs to be built correctly. 
2. After Indexing, Wabbajack will make its first pass at all of the files and .meta files in the downloads folder you specified. It will check to make sure that it can access those files from the internet and that they haven't been changed or removed. This is the most common point of failure for modlist compilation. Note that even if it does fail here, Wabbajack will still provide you with useful information in its log. It will tell you which files are problematic and why. These are the most common reasons why it would fail at this step:
   1. A file(s) is no longer available from the internet.
   2. Your internet connection has failed.
   3. A file(s) is not from the list of approved sources. You can check this list [here](https://github.com/wabbajack-tools/opt-out-lists/blob/master/ServerWhitelist.yml) and also request that things be added to it. For more information about getting things added to the list, it's best to head to the [Wabbajack Discord server](https://discord.gg/wabbajack).
   4. A file(s) has been rate-limited (usually a file hosted on Google Drive) and is temporarily unavailable.
3. Next is the actual compilation part of the process. During this step, Wabbajack will compare everything it Indexed earlier to what is actually installed in the modlist. If it finds that a file has been modified from what has been indexed, it will create a patch to transform the file into what the modlist is expecting. This happens frequently with mods such as BodySlide, which creates new versions of existing files that have been modified from their original state. At this point, Wabbajack will also take into account any mods that have a [Special Flag](https://github.com/wabbajack-tools/wabbajack#special-flags) and either include or exclude those files as needed. This is also when BSA handling is done - if a BSA has been modified/created/unpacked, Wabbajack will account for that at this point. There are a few less common points of failure during this step of the process:
   1. BSA issues - Wabbajack is missing the files it needs to create/modify/unpack a BSA.
   2. If there are any files that cannot be sourced from the downloads folder.
   3. If a file is modified, added, or removed while Wabbajack is working with it.
4. Wabbajack will now take another pass at all of the files and .meta files in the downloads folder you specified. Because the compilation part of the process can take an exceptonally long time (especially for first-time compiles), Wabbajack needs to check again to make sure nothing has changed in the time it took to finish step 3. All of the same points of failure from Step 2 apply here as well.
5. Finally, Wabbajack will do any back-end cleanup it needs to do and produce the finished Wabbajack installer file. This file is placed in the Output folder you specified earlier.

If you encounter any issues with the compilation process, definitely head to the [Wabbajack Discord server](https://discord.gg/wabbajack) and ask for assistance in the #modlist-development-help channel.

## Finishing Up

Once Wabbajack reports that compilation is complete, you're done! The Wabbajack installer file can be uploaded to the internet and shared, or stored if you're just making a backup of a specific load order.

You'll see that Wabbajack actually created 3 files: The installer file, a Meta file, and a Manifest file. The installer is what users will load into Wabbajack to install the list. The meta file contains metadata about the installer - install size, number of files to download, etc. The Manifest is a powerful file that can be loaded into Wabbajack's website on the [Manifest Viewer](https://www.wabbajack.org/#/modlists/manifest) to view a complete listing of every file Wabbajack will download as part of the installation process.

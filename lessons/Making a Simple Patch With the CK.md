# Introduction to the Creation Kit - Making a Simple Worldspace Patch

Hey, we haven’t touched on anything in the CK yet, have we? Well, that certainly can’t stand. Let’s get in there!

This time, we will familiarize ourselves with some basic controls in the Render window, learn a few keyboard shortcuts, and make a pretty easy and effective patch for some worldspace problems. But we can’t jump straight into the Creation Kit - we need to do a few things beforehand.

First thing’s first: you need [this](https://www.nexusmods.com/fallout4/mods/47373/). Download it and drop the .ini file into your Fallout 4 folder, right next to the CreationKit.exe.

If you don’t have the Creation Kit installed yet, you need to do that through the Bethesda Launcher. It’s easy and free, so go grab that.

Next, we need to know what we’re making a patch for, obviously. That’d be [Boston Natural Surroundings v2.2](https://www.nexusmods.com/fallout4/mods/30673) and [Minuteman Watchtowers](https://www.nexusmods.com/fallout4/mods/30363).

Make a new profile in MO2. If you don't know how to do this, please see [Introduction to Mod Organizer 2](https://github.com/LivelyDismay/Learn-To-Mod/blob/45924ba2654319ba868cfa69495fb6ff3c9bfa44/lessons/Introduction%20to%20MO2.md).  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro1.png)  

![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro2.png)  

Name it what you want. I like to name it the same I’ll be naming my future patch, so this will be mine.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro3.png)  

Select this profile in MO2.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro4.png)  

Click this icon and select Install Mod.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro5.png)  

Find Boston Natural Surroundings in your downloads folder and double click it.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro6.png)  

BUT WAIT! We need to rename it first. We DO NOT want to overwrite our regular version of BNS, because we’re going to be making changes here so the CK works properly with it. More details on this in just a moment. Rename it what you like - I choose to tack the word “Previs” on the end of mods when I need to do this exact thing.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro7.png)  

Do the same with Minuteman Watchtowers. Install and rename it, then activate both of your new mods.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro8.png)  

Now we need to launch xEdit and load all modules.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro9.png)  

Wait until the right pane says `Backrground loader: finished`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro10.png)  

Expand Boston `Natural Surroundings.esp` and select `File Header`. In the right pane, double click next to `Record Flags` and check the box next to `ESM`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro11.png)  

Do the same with Minuteman Watchtowers.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro12.png)  

Exit xEdit and save your plugins.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro13.png)  

So why did we just do this? Well, the CK really doesn’t like plugins that aren’t ESMs or ESM-flagged, and will often just strip all the references out of anything you make using them as masters. This leaves you with errors and garbage data instead of actual, useful changes. **It is best practice to ESM-flag any plugins you’re making patches for in the CK**. The new release of F4 CK Fixes does address this, but it has a few other issues, so I'm slightly hesitant to recommend it at this point in time.

You can see now they’re **bold** in your plugin list. That means they’re ESM-flagged. Perfect! Now we can launch the CK.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro14.png)  

When the CK loads up, click File > Data.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro15.png)  

Select the two mods you’re making a patch for. DO NOT select an Active File. Remember, we are making a new patch from scratch here, not editing an existing mod.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro16.png)  

Wait for the CK to load. This may take a while, depending on your hardware. The CK also really doesn’t appreciate it if you alt-tab out to other windows. Consider yourself warned.
Welcome to the Creation Kit! Feel free to look around and adjust the windows to your liking. When you’re ready, let’s just dive right in.

In the Cell View window, change the World Space section to read `Commonwealth`. This list may take a moment to populate.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro17.png)  

The author of Minuteman Watchtowers conveniently made his watchtowers in new cells prefixed with `000`, so they’re right at the top of the list. Nice! Double click the first one, and - you guessed it - wait for a little while until the Render Window loads up the cell.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro18.png)  

You’re going to “spawn” into the cell staring at the dirt. This is just the default position of the camera in the CK. *Get used to it*. Let’s take a moment to familiarize ourselves with the camera controls. The obvious starting point is to make it so we aren’t staring at the fuckin floor anymore.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro19.png)  

Make sure the Render Window is the active window in the CK (like changing tabs in your internet browser), hold `Shift` and move your mouse around. Congratulations, you learned how to rotate the camera and look around. Neat!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro20.png)  

Scroll the mouse wheel in and out to zoom the camera...in and out. Who would have guessed.

I see a watchtower! Let’s head over there. Just point your camera at it and scroll your mouse wheel up until you get closer.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro21.png)  

That’s better. But I feel kind of close to the ground, and I would prefer an aerial view. Hold `Space` or the middle mouse button, and move the camera around. This lets you change the camera view without changing the angle.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro22.png)  

Now we have an aerial view of the tower, and there’s a GIANT GODDAMN TREE GROWING THROUGH THE MIDDLE OF IT. Obviously, this is what we’re here to fix. Click that tree!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro23.png)  

Press the `Delete` key. YEET! It’s gone! Let’s look around a bit for more trees. Hold Shift to look around a bit more.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro24.png)  

Whoa, hey, you just spun around in a big circle instead of looking around just then, didn’t you? Well, that’s because, as far as the CK is concerned, you still have that tree selected. So you’re spinning in a big circle around that tree.

Press `D` to deselect the tree, then press `Shift+F` to reset the camera back to its neutral state. **This is insanely useful**. Try to make it reflexive for anytime you need to deselect or delete an object. Spinning in giant circles can throw you off real quick.

Anyway, now that the camera is reset, practice moving the camera around to see if any more trees need to be deleted.

Just this one, in my opinion. It’s clipping into the steps. Get rid of it!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro25.png)  

Back to the Cell View window. You can see that `000MinutemanTower01` now has an asterisk `(*)` next to it. This is showing us that we edited this cell. Nice. Anyway, double click the second tower and wait for the Render Window to load the cell.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro26.png)  

Looks like two trees I’m not really fond of this time around. Onward to the third tower! And the fourth, fifth, and so on. Keep going until you feel you’ve removed all the problematic trees around all the towers.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro27.png)  

When you feel you’ve got them all, go to File > Save.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro28.png)  

Name it what you like, and don’t forget to type in the .esp file extension. You may also think this looks a bit strange. It shows us saving to the Fallout 4\data folder, but we launched through Mod Organizer 2, so what gives? Well, the Virtual Directory makes the CK “think” we are launching from the Fallout 4 folder, so saving it here will *actually* save the plugin into your MO2\overwrite folder. Perfect!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro29.png)  

Go ahead and close the CK. Back in MO2, you can see the new plugin at the bottom of the load order, and I also very politely opened up my Overwrite folder to show you that it did indeed get saved there as opposed to your game’s data folder. Excellent!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro30.png)  

But, we are not done quite yet. Activate your new plugin, then launch xEdit QAC. This stands for QuickAutoClean, and we are doing this for one reason: xEdit will automatically change the trees we deleted from `Deleted` to `Initially Disabled`, and move their Z coordinates to `-30000`. This is the “safer” way to remove placed objects, just in case anything else references them. Deleted references are bad, and may crash your game seemingly randomly.
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro31.png)  

When QAC opens, select your new plugin. You’ll see it also activates all the masters for that plugin. Only clean one plugin at a time! If you need to clean multiple plugins, clean one, close QAC, then launch it again to clean the next one.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro32.png)  

It’ll tell you when it’s done. Go ahead and close the program - no need to save this time, it autosaves itself when the cleaning is complete.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/d0363c9399ed72cded7978fd08d0720edbdc02eb/images/ckintro33.png)  

Go check out your watchtowers in-game. So nice and clean! No more trees growing through them at random! Fuck yeah.

The CK can be really intimidating for a lot of people, so I genuinely hope this simple exercise has shown you that it doesn’t have to be the scary monster it’s been built up to be. Of course, it can get *much* more complicated depending on what you’re doing, but fixing worldspace issues like this is generally as easy as what we just did...except when it comes to broken previs/precombines. I’ll cover that at a later date because, quite frankly, it’s a time-consuming pain in the ass. But we’ll get there!

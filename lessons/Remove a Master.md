# How To Remove a Master Requirement From a Plugin

---

### Scenario 1

Today, I want to remove the `Restore Power Armor Frames` mod. It was a good run, but ultimately, it's a little bit buggy and is a bit overpowered.

My first step for this is simple: break shit!

Filter for the mod at the bottom. Select `Restore Power Armor Frames` in the left pane. See the blue line in the plugin scroll bar on the right? That's showing me where the plugin is for the mod I have selected.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  

Deactivate it. Now you have missing master warnings. Cool! This tells me what plugins require Restore PA Frames. In this case, just the sorting patch.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster2.png)  

Now I could delete the mod and rerun the sorting patch, but...well, you wouldn't learn anything! So let's remove it the old-fashioned way.

Reactivate the Restore PA Frames mod to get rid of the missing masters warning.

Launch xEdit. Load all modules.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster3.png)  

Wait for the messages on the right to say `Background loader: finished`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster4.png)  

Scroll all the way to the bottom, where your Complex Sorting plugin is located. Right click and select Apply Script.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster5.png)  

Today we are using the Report Masters script. Use the Filter to find it, or scroll through the list.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6760faa7550de2779e1085d011862c3b0de5d830/images/removemaster17.png)  

This pulls up a list of all the masters that the Sorting plugin has.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster6.png)  

Find and select RestorePAFrames.esp. Feel free to use the Search bar at the top as a filter if needed.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster7.png) 

Wait until the messages say `Done Applying Script`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster8.png)  

You'll see the references listed there as well - those are the records which the Sorting plugin needs from RestorePAFrames.esp. In other words, this is what needs to go away.

Control-double-click the ID next to `NOTE` to jump to that record.

This record is simply categorizing the settings holotape. Since this is a record created by RestorePAFrames.esp, is not an override, and does not contain any data or references from any other mods, we can just outright delete this record from the sorting plugin.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster9.png)  

Simple.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster10.png)  

No more override.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster11.png)  

You can go back to the Messages tab at the bottom of the right pane in xEdit to check other references caught by the Report Masters script. In this case, that was the only one. If you'd like to be sure there are no others, feel free to run the Report Masters script on it again.

As you can see, there are no more references.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster12.png)  

Right click your sorting plugin, and select `Clean Masters`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster13.png)  

You'll see the `File Header` has turned bold.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster14.png)  

This means something changed - which is good, since that's where the masters are all listed.

Close xEdit and save.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster15.png)  

Now let's try this again: disable the RestorePAFrames.esp in your load order.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster16.png)  

No more missing master warning! You can safely delete this mod from MO2.

This is a very simple example of this. Let's cover one more.

---

### Scenario 2

I have a missing master in my MO2 right now, but I deleted the mod itself, so I no longer have the plugin. What can I do about that?

Well, obviously I could redownload the mod, activate it, then follow Scenario 1 again, but we wouldn't learn anything! Instead, let's make a Dummy Plugin. You can do this a few different ways, but there are two main ways to accomplish this.
 - Use Wrye Bash, which has an option to generate dummy plugins for missing masters.
 - Use the Lively Method, which... quite obviously, we are going to do here today.

The end result here will be the same. The only real difference is my "hacky" method is a bit faster, and doesn't require downloading/running another tool. More streamlined for us here in xEdit lessons, ain't it?

So, step one: find a plugin. Preferably a small one. For this example, I'm going to find any random patch I've made.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster17.png)

Copy any one of these (I'm just going to use the first one), then paste it literally anywhere else.
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster18.png)
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster19.png)
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster20.png)

Now we need to know the name of the master we need. Back to MO2 and check that Warnings tab, it'll tell ya. In this case, I need a dummy plugin for `CROSS_GoreCrits`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster21.png)

So let's rename our duplicated patch.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster22.png)

And for this, I'm just going to pop it into my MO2's Overwrite folder. You can put it anywhere you like, as long as it shows up in your MO2 plugin list.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster23.png)

Head back over to MO2 and press `F5` to refresh it. Your new dummy plugin will show up at the bottom of your plugin list here. Don't forget to activate it!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster24.png)

Now we don't have a missing masters warning. Go ahead and launch xEdit. As usual, wait for the Background Loader to finish, then scroll all the way to the bottom.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster25.png)

You may notice something here immediately. We had our dummy `CROSS_GoreCrits` plugin activated at the end of our load order in MO2, but in xEdit, it loads it right above `M8r Complex Sorter`.  

Why is that? Well, I know a lot of people get a little confused by this, but it's really quite simple. If your MO2 plugin list and xEdit's plugin list don't match, then your MO2 list is wrong. xEdit loads plugins the way the game engine will, meaning Deliquent Masters (or, plugins that are out of order) will be loaded above the files requiring them. Since `M8r Complex Sorter` requires `CROSS_GoreCrits` as a master, GoreCrits is loaded above the M8r plugin. Nice!

Now we are basically back to Scenario 1, so let's run the `Report Masters` script on `M8r Complex Sorter`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster26.png)
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster27.png)

Use the filter here to make your life easier, if you want.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster28.png)

All done! 
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster29.png)

Unfrotunately, since we are using a dummy plugin, this record doesn't actually exist, so we can't use the FormID to jump to it. We will have to find it by EditorID. But that's no problem! We can use the Record Signature (ARMO) to make things easier, and just sort by EditorID at the top so everything is alphabetical. 
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster30.png)

You'll notice this record has no overrides and is in *italics*. There are no overrides because there's nothing to override, due to us using a dummy plugin instead of the "real" plugin. The italics are because the FormID is being read as "injected" (see how `M8r Complex Sorter` has a Mod Index of D3, but the record here is `FE 261`? That's what injected means.).

Anyway, long story short, we can just delete this record.
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster31.png)

Then go ahead and Clean Masters, since that was the only thing referencing `CROSS_GoreCrits` in our M8r plugin.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster32.png)

Close xEdit and save your plugin. Make a backup if you want.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster33.png)

Now we can get rid of our dummy plugin and we don't have a Missing Masters warning anymore! Yay!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/removemaster34.png)

Go ahead and delete that dummy plugin from Overwrite, our job is done here.

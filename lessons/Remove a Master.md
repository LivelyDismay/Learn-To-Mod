# How To Remove a Master Requirement From a Plugin

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

This is a very simple example of this. Removing masters from other types of records, like Leveled Lists for example, require you to remove specific entries from the records in question, as opposed to outright deleting the entire record. We can cover that at a later date when I do a more in-depth look at Leveled Lists.

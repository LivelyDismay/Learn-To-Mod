# How To Remove a Master Requirement From a Plugin

Today, I want to remove the `Restore Power Armor Frames` mod. It was a good run, but ultimately, it's a little bit buggy and is a bit overpowered.

My first step for this is simple: break shit!

Filter for the mod at the bottom. Select `Restore Power Armor Frames` in the left pane. See the blue line in the plugin scroll bar on the right? That's showing me where the plugin is for the mod I have selected.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  

Deactivate it. Now you have missing master warnings. Cool! This tells me what plugins require Restore PA Frames. In this case, just the sorting patch.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  

Now I could delete the mod and rerun the sorting patch, but...well, you wouldn't learn anything! So let's remove it the old-fashioned way.

Reactivate the Restore PA Frames mod to get rid of the missing masters warning.

Launch xEdit. Load all modules.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  

Wait for the messages on the right to say `Background loader: finished`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  

Scroll all the way to the bottom, where your Complex Sorting plugin is located. Right click and select Apply Script.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  

Today we are using the Report Masters script. Use the Filter to find it, or scroll through the list.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  

This pulls up a list of all the masters that the Sorting plugin has.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  

Find and select RestorePAFrames.esp. Feel free to use the Search bar at the top as a filter if needed.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  


![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  


![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  


![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  


![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  


![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  


![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  


![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  


![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6134950cc7345a5fb8291b3b15de445292e40bf3/images/removemaster1.png)  

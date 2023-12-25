# Flagging Plugins as ESL: How-To, Pros, and Cons

Check out my [One Minute Modding](https://www.youtube.com/shorts/maAWv4CCkOk) video on simple ESL flagging, or read on it you prefer text format.

---

So you've been following my tutorials for a while. You added a bunch of mods, you patched them, you ran the Item Sorting script, and now...your game won't load, or your MCMs keep reverting back to their defaults, or your mods are acting strangely. Turns out there's a plugin limit of 254 ESMs+ESPs. You can view how many you have in MO2 if you just click the Plugin count:  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl1.png)

See that one near the bottom? ESMs+ESPs? If that's over 254, your game is broken. *But I want more mods, Lively! You have almost 600, why can't I just add 20 more?* I have heard your cries, and I am here to help.

Your first thought may be, "Well, I've heard of people merging plugins. Why don't I just do that?" Merging is an outdated method. It's a bit sloppy, it's difficult to work with, and one of the only benefits is that it *looks* cleaner in your plugin list (the other being that it can reduce the number of ba2 archives being loaded, but that's a conversation for another day).

ESL flagging is the future. Or...the present. Why is it better than merging, you ask? Easy: it only takes a few clicks, and ESL-flagged plugins **DO NOT** take up one of the 254 slots in your plugin count. ESLs are all kinda pseudo-merged into the 255th slot at runtime. Neat! Let's do that, then!

Launch xEdit.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl2.png)

Load all modules.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl3.png)

Wait until it says `Background loader: finished`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl4.png)

Right click anywhere in the left pane and select `Apply Script`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl5.png)

We are running this script: `Find ESP plugins which can be turned into ESL`. Use the filter at the top to find it if you like, or scroll through the list of available scripts.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl6.png)

Click OK, and watch your Messages in the right pane go absolutely crazy. It won't take long before it says it's finished.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl7.png)

You can see right away there are only two kinds of results:  
1.  Can be turned into ESL by adding ESL flag in TES4 header  
2. Can be turned into ESL by compacting FormIDs first, then adding ESL flag in TES4 header  

The first one is incredibly simple, so let's start with that. The last message in my right pane says the following:  
`[E9] M8r Complex Sorter.esp
	Can be turned into ESL by adding ESL flag in TES4 header`

So let's do that. Select `M8r Complex Sort.esp` in the left pane.
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl8.png)

Double click in the `Record Flags` field in the right pane.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl9.png)

Check the `ESL` box.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl10.png)

This plugin is now flagged as an ESL, so it no longer occupies one of your precious 254 plugin slots.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl11.png)

And...well, that's it. Seriously. A few clicks, and that plugin is now ESL-flagged. So let's have a look at the second version: compacting FormIDs.

First, I'm sure you're asking why some plugins can be flagged outright, and why others need to have their IDs compacted first. The answer is simple: ESL records can only occupy a specific range of IDs - from FExxx000 to FExxxFFF. In Skyrim, however, the range is slightly different: FExxx800-FExxxFFF. In any case, compacting the FormIDs will force all the records to be within this range so that you can safely ESL flag it.

A quick sidenote: if you compact FormIDs, **you cannot continue an ongoing save with that mod**. You absolutely cannot change formIDs mid-save. Ever. No way around it.

Moving on...

In the right pane, make sure the Messages tab at the bottom is active. Above the entry for M8r Complex Sorter.esp is this:  
`[E7] SS2_XDI Patch.esp
	Can be turned into ESL by compacting FormIDs first, then adding ESL flag in TES4 header`

Let's do it! Find the `SS2_XDI Patch.esp` in the left pane. Right click it and select `Compact FormIDs for ESL`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl12.png)

You'll get a message reiterating what I just said above: this WILL break any ongoing save you have with this plugin active. Click Yes.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl13.png)

You'll get a message saying it's done in no time.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl14.png)

Now we just treat it the same way we did `M8r Complex Sorter.esp`: double click the Record Flags and check the ESL box. Simple!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/ea266971c5ba254dd1c8f05a99c19d11e9fe2711/images/esl15.png)

With this method, you can go wayyy beyond the 254 plugin limit. The (theoretical) limit for ESL plugins is 2048, if I recall correctly, but let's face it: the engine will likely curl up and die long before you ever reach that limit.

Enjoy your new mods!

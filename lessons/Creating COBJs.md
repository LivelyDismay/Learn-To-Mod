# Constructible Object Records

"Lively, you talk about COBJs constantly and that's all well and good, but there's just one problem: *I don't know what the hell a COBJ is.*"

I got you, fam.

Today we will be using Fallout 4 + all DLCs, in conjunction with [Lively's Keyword Resource](https://www.nexusmods.com/fallout4/mods/51510) and [Whisper's Standalone Workbenches](https://www.nexusmods.com/fallout4/mods/41832). Let's just jump right in, shall we?

Launch xEdit.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj1.png)

Load all modules.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj2.png)

Wait until it says `Background loader: finished`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj3.png)

Now you have a decision to make. Go through whatever records you want in whatever mods you want, and figure out what exactly you want to make craftable. For the purpose of this exercise, I've chosen the Fragmentation MIRV grenades from Nuka World. They're extremely powerful, extremely rare, and only three of them exist in the base game. I'm here to have fun and blow people up, dammit! I want more! **I'll just make more, then!**

In case you aren't aware, I am just...incredibly lazy. Seriously. I find the laziest possible way to do things, because they're fast and they work for me. So let's be lazy together.

Type `06033905` into the FormID search bar in the top left and press Enter. You'll jump down to the record for the grenaes.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj4.png)

Right click the record in the left pane and select `Copy as override into...`  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj5.png)

Select a new ESP flagged as ESL and select OK.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj6.png)

Name it whatever you want and press OK.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj7.png)

Now we have a copy of this. Neat! Spoilers: *we don't need this record.* But now I have a new patch plugin to work with! Yayyyy. Right click your new plugin in the right pane and select `Jump to`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj8.png)

You'll see the left pane has jumped down to our fancy new plugin. Nice. Right click that bad boy and select `Add`, then `COBJ - Constructible Object`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj9.png)

Now we have a new category here.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj10.png)

Right click the new category, select `Add`, then `COBJ - Constructible Object`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj11.png)

"But we JUST DID THAT." I know. The first time was to create the category for the new plugin, and the second time is to create a new record inside that category. Just roll with it and stop yelling at me.

The default FormID is fine. Just click OK.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj12.png)

Right click the `EDID` field in the new record and select `Add`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj13.png)

Now it's white! Right click it again and select `Edit`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj14.png)

Name it...almost whatever you want.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj15.png)

Let's quickly go over some rules and basic naming conventions for EDIDs. First, it's a good idea to use your own unique prefix - you'll see I often use liv, lkr, lwc, and lws, depending on what it is I'm making. This is to easily use a filter (usually in the Creation Kit) to find your own stuff. Next you'll notice `co`, which is pretty standard vanilla naming for Constructible. Then `weap` which is telling me it's a Weapon. Then the name of the weapon I'm crafting. So with a quick glance at just the EDID, I can see this is a COBJ I made to make MIRV grenades. Lastly, no spaces. EDIDs should all be one word, or have underscores, but they can't have spaces.

In other words, feel free to name your EDID `CatsPlayingSoccer` but don't name it `Cats Playing Soccer`.

...anyway, moving on.

Next, right click in the Components field and select `Add`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj16.png)

Components are what the player will need in order to craft this thing. You can have as many or as few components as you like, and you can use pretty much anything in the game - or anything from any mod, if that mod is listed as a master for this patch. Since these grenades are so powerful and so rare, normally I would to make them a bit more difficult to craft. But for this lesson, I won't worry much about the actual components or balance here.

Let's start simple and say you're upgrading a grenade rather than crafting a new one. So, add a regular grenade to the components.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj17.png)

Add another component!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj18.png)

Just keep adding stuff until you're happy with your recipe. Easy. Feel free to change the amount of each component needed via editing the `Count`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj19.png)

Do note that I don't particularly care about this, I'm simply picking random crap.

If you'd like to add Conditions to this (such as Perk Requirements, Quest Completion checks, or anything like that), now's the time to [read up on my Conditions lesson](https://github.com/LivelyDismay/Learn-To-Mod/blob/2b099dfce3c096f82ddd85e973538d18c14cf304/lessons/Conditions.md).

For the `Created Object`, right click and `Add`, then select the object you want to be created when you craft this recipe - in this case, the MIRV grenade.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj20.png)

Now, right click in the `INTV - Data` field and select `Add`, and change the `Created Object Count` to 1 (or however many grenades you want to be given to the player when this recipe is crafted).  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj21.png)

We're almost done - the last things we need are the `BNAM`, which dictates where this recipe is crafted, and the `FNAM`, which is the category this recipe will appear under. Since we are using Standalone Workbenches, we need this mod to be a master for this patch. Right click our plugin in the left pane and select `Add Masters...`.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj22.png)

Select both Lively's Keyword Resource and Standalone Workbenches. Note: since we originally created this patch via copying a record from Nuka World, that DLC's esm is already listed as a master. Yay laziness!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj23.png)

Exit and save your patch.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj24.png)

I do this after adding masters because xEdit is finicky and doesn't like immediately allowing you to use assets from masters you just added. Closing and relaunching the program solves this problem and only takes a few seconds, so let's do that.

First, activate your new patch in your load order. Then launch xEdit, load all modules, wait for the background loader to finish, and scroll all the way back down to our fancy new COBJ.

You'll see we now have the masters we need in the File Header.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj25.png)

Anyway, head on down to that COBJ and add a BNAM. Change the BNAM to the workbench you want it to be crafted at - Whisper's benches all start with `wsw`, to make it easy.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj26.png)

Now add an FNAM and select a keyword. All of my keywords start with `lkr`, and are further sorted into subcategories per workbench. So in this case, `lkr_exp` will jump you to the section you (probably) want.  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj27.png)

If you'd like to make your own category, then you'll need to add your own custom keyword for a new recipe filter. Lucky for you, [I wrote a thing for that, too](https://github.com/LivelyDismay/Learn-To-Mod/blob/2b099dfce3c096f82ddd85e973538d18c14cf304/lessons/Keywords%20Intro.md)! I got you covered.

That's it! You can now craft fragmentation MIRV grenades at the Explosives Workbench under the `GRENADES - SPECIAL` category as long as you have Demolition Expert rank 4 and you've completed the Power Play quest. Wooooo!  
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/6cfadd95684d94ee42c561d4422ec856086d7031/images/cobj28.png)

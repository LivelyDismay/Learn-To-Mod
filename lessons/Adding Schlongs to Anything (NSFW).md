# Adding Schlongs to Anything

So you've got a nice friendly _Skyrim Special Edition_ Wabbajack modlist and you're just dying to see fully functional and anatomically correct schlongs on all males you loot. This is actually far more complicated than getting the females naked, which, as far as I can tell, is the opposite of real life.

There are **four steps** to this process, and **one optional _advanced_ step.**

1. Configuring _XMPSE32_ to be compatible with _Schlongs of Skyrim_.
2. Installing _Schlongs of Skyrim._
3. Installing a _Schlongs of Skyrim_ compatible male body texture.
4. Arranging the mod(s) properly in MO2.

**Advanced:** Copying the _Schlongs of Skyrim_ compatible male body mesh and texture over to _all_ NPCs.

## Configuring _XPMSE32_ to be compatible with _Schlongs of Skyrim_

The first step is making sure your male skeleton has a "bone" (huh huh huh) to attach the schlong to. This is accomplished by reinstalling a skeleton mod called _XMPSE32_ which is in almost every Wabbajack list. Find it, right-click, and choose this...
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/SOS.everywhere.01.png)

Now you'll have a butt-ton of options. Unfortunately these will vary for each modlist installation so some tweaking may be necessary, I recommend you experiment. I'll give the most common selections here.

Physics extensions depend on whether CBPC is installed. Search for it and install it if it's there. Otherwise choose None.
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/SOS.everywhere.02.png)

Now you'll wanna go ahead and hammer through the next six screens until you get to this one...
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/SOS.everywhere.03.png)

Obviously you'll want _Schlongs of Skyrim_ and nobody in their right mind still uses _Joy of Perspective_ so be sure not to pick that.

Just click next now all the way through to finish at the end.

## Installing Schlongs of Skyrim

The next step is to download _Schlongs of Skyrim_ from _Lover's Lab._ I'm not gonna link it because Github is kinda picky but it's very easily found. Be sure to get the SE version.

Now install the mod.

First choose your body type. I recommend Default because BodyBuilder just looks ridiculous, wouldn't you agree?
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/SOS.everywhere.04.png)

The next option is really irrelevant given that the body texture that comes with SOS is garbage, so here's the hairy version for some more hilarity.
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/SOS.everywhere.05.png)

On this page, choose how much "schlong variety" you want. Average is actually small, regular is big but thin, and muscular is girthy. There's no harm in installing all three, the mod will choose among them for each NPC.

I can't show you pictures because this is a family-friendly website, mister, so look at this grid instead.
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/SOS.everywhere.06.png)

Be sure **NOT** to install the skeletons because we're using be using XMPSE32 for those and do **NOT** install the Shop as it will add worldspace edits I don't want to deal with right now.

## Installing a _Schlongs of Skyrim_ compatible male body texture.

You could totally just quit here if you're only worried about your own wanger and you don't care how ugly you are. If this is not true, you'll want [Tempered Skins for Males.](https://www.nexusmods.com/skyrimspecialedition/mods/7902) Be sure to grab the "SOS Full" version obviously.

Install the mod, but I'm not gonna show pics because they're kinda iffy and they're all honestly personal preference. Explore that latently gay self with extremely specific details about how your hot man bods look!

## Arranging the mod(s) properly in MO2.

Strangely enough, these mods are extremely unlikely to have any real conflicts with any ESPs in your list so the left pane is more important. You'll want _Schlongs of Skyrim_ to overwrite (be down below) anything referencing male bodies in your modlist, and _Tempered Skins_ just below that. _XPMSE_ needs to be after all of these. 

Arrange the left pane accordingly, and in the right pane, move _Schlongs of Skyrim - Core.esm_ up a few notches. It will automatically jump to where it needs to be. Magic!

As for the various schlong "types" you can leave those at the end.

## Advanced: Copying the _Schlongs of Skyrim_ compatible male body mesh and texture over to _all_ NPCs.

Most Wabbajack modlists use male NPC overhauls and a lot of these use underwear by default. This is by far the most annoying part of this whole process. If you want not just all the men you loot to have schlongs, but all the people you talk to to have schlongs as well, like say if you want to do a hilarious `unequipall` on them or god forbid have sex with them, you will need to find _every instance_ of the following meshes in your modlist and overwrite them with the ones from _Schlongs of Skyrim_...
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/SOS.everywhere.07.png)

You will also need to do the same for the textures from _Tempered Skins_...
![alt text](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/images/SOS.everywhere.08.png)

Protip the easiest way to do it is to use a decent search tool like _Everything_ and search the entire MO2 directory for instances of "malebody_1.nif" and "malebody_1.dds". Copy all the related files over to the directory they are in. There might be a lot of them!

And that's it! After all this you may have trouble launching _Skyrim_ because some jerk intentionally made it hard for you to add mods. Pester Lively for a tutorial on how to set plugins to ESL so you'll have room for this dumb stuff!

Sayonara!

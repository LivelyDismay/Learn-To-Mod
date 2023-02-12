2023/02/12

Version 6.3.5 (accidentally skipped 6.3.4 because it was just a recompile for the latest Wabbajack update)

Removed Baka ScrapHeap.  
Edited Buffout 4's .toml to change MemoryManager to `true`.  
Some ini edits to see if the blue landscape is resolved (if not, it's either a shadow problem or a weather problem, in all likelihood).  
Edits to `Lively's Tweaks.esp` to revert Dead Body Cleanup and Cell Cleanup timers to vanilla (to reduce possible save bloat).  
Removed `CROSS_GoreCrits.esp` as a master for the CC profile's Complex Sorter outputs. There is also a [write-up to do this yourself](https://github.com/LivelyDismay/Learn-To-Mod/blob/main/lessons/Remove%20a%20Master.md) if you want to learn how.  

---

2023/01/22

Version 6.3.3

Recompiled on WJ v3.0.6.0. Hopefully fixes installation issues people are having since yesterday. Mild changes while I'm at it:  

Renamed Venom Ammo Change gloves from Courser Crusher.  
Renamed Venom Ammo Change Power Armor from Courser Crusher.  
Fixed at least one instance of Minutemen possibly spawning naked. We will keep an eye out for more.  
Removed a bed from Beantown Brewery. Yes I finally remembered.  

---

2022/12/31

Version 6.3.2

Happy new year.

Updated ECO - Equipment and Crafting Overhaul.  
Updated 4est Complex Sorter Enhancements.  
Updated m8r's Complex Sorter.  

Changes to some patches (such as ECO Patchwork.esp).  
Some stuff to maybe help HQ run more smoothly? We will see, I guess.

---

New sorter outputs for both profiles.

2022/12/26

Version 6.3.0

A quick note: this should technically require a new save, but these are all the things I've done to my own modlist during the filming of [my YouTube series](https://youtu.be/YtAwqBjWo24), and I haven't started a new save, so...take that as you will. If you do plan to update and keep playing a save, I'd recommend using the `coc sanctuarybasementjahani` command, waiting for 30 days, saving, closing the game, then updating the modlist. This will teleport you to the small basement in Sanctuary and essentially clear the cache of whatever is loaded in any other cell, effectively making sure the game isn't loading anything else. This will, however, reset all enemy spawns and such, so...you just have to deal with that. Same as I did on my series, if you've been watching.  

Other than that, this is a pretty simple update. Removing some issues, fixing some issues, and most importantly, updating SS2 stuff. **If you have not played newer versions of SS2, you need a Recruitment Clipboard to hire people for HQ.** So if you're already beyond that point in the SS2 questline, either console yourself the item (`help recruitment 4 weap`, then add it via `player.additem <id> 1`, or it should be on top of Theresa's terminal in HQ. Consoling is the easier method...  

This SS2 update also includes a hotfix from last night to address an issue with an infinite loop in the coding for the holotape tools. This fix should run automatically for you, so no extra steps required for you guys. You may or may not get a one-time pop-up stating that the fix ran and cleaned your save (I only used the test version from last night, not the one included in the mod),

Added Workshop Plus.  

Updated Sim Settlements 2.  
Updated Sim Settlements 2 Chapter 2.  
Updated Workshop Framework.  

Removed You and What Army.  
Removed Cross Crit Gore-verhaul.  

Renamed `Cinematic Lensflares.ba2` to `Cinematic Lensflares - Textures.ba2`.  

---

2022/07/11

Updated Active Effects on HUD.

Updated Better Companions - All in One. Removed a handful of custom tweaks to BC-AIO from Better Companions - Lively's Tweaks.esp.

Minor load order adjustments.

---

2022/07/10

Updated Readme.

Updated F4SE.  
Updated Heather Casdin.  
Updated Wasteland Heroines Replacer - Heather Casdin.  

Updated Game Folder Files. **Please copy these over to your game directory again if updating.**

Removed Randomized Valuables Redux.  
Removed Human Grab Attacks.  
Removed Workshop Plus.  

---

2022/06/02

Version 6.1.1

Slight update to This is Trash.  
Fixed various typos that were bothering me.  
Fixed Drumlin Diner.  

---

2022/05/19

Version 6.1.0

Updated Sim Settlements 2.  
Updated SS2 Chapter 2.  
Updated Workshop Framework.  
Updated Rise of the Commonwealth for SS2.  
Updated Creative Perks Plus.  
Updated FallUI - Map.  
Updated FallUI - HUD.  
Updated FallUI - Confirm Boxes.  
Updated FallUI - Workbench.  
Updated FallUI - Inventory.  
Updated Portable Junk Recycler Mk2.  
Updated Heather Casdin.  
Updated MCM Settings Manager.  
Updated SS2 - XDI Compatibility Patch.  
Updated 4estGimp - M8r98a4f2's Complex Item Sorter Enhancements.  

Added SS2 Settlers at Play.  
Added ECO - Old Time Religion patch.  
Added FallUI - Icon Library.  
Added FIS - The NEW FallUI Item Sorter.  
Added Atom Cats Drag Race Start Fix.  

Removed DEF_UI Iconlibs Rescaled and Fixed.  
Removed Flicker Fixer.  

Reran sorter outputs.  
WF Witch outfit from Far West Minutemen will no longer spawn.  
Restored all ROTC plans so you can build them without restriction. Untested.  
Removed doubled Psychotats recipe.  
Typo fix in Heavy Gunner rank 2 description.  
Bug fix to Lively's CC - VR Workshop - Desert Island.esp (CC Profile only).  
Edited perk descriptions for Fortune Finder ranks 2 and 3.  
Added new keyword for WeaponTypeSubmachineguns; edited Heavy Gunner rank 1 to reflect this. So what's that mean? Any weapons in the Submachine Guns category in the Weaponsmith Workbench will benefit from Heavy Gunner's Submachinegun-specific buff.  

Known issues:  

One house at the top of the hill in Concord is invisible, causing culling issues.  
Presets have default hair.  
Claudia (12047d77, 12047d55) spawns naked.  
Heather Casdin and Vault 494 use the same radio frequency.  

Notes: 

This is Trash was rebuilt from scratch. That's why you have two of them in the left pane. The new one will (eventually) completely replace the old one. When I stop being so lazy.   
Updates are never mandatory. This version of Magnum Opus has been very thoroughly tested by myself and a few dozen others, so bugs should be extremely minimal. In 26 hours of playtime, I had one crash that I could not reproduce or diagnose.  
The known issues are so minor that I'm finally comfortable releasing this into the wild. Thanks for your time.

---

2022/05/12

Version 6.0.0 Beta 3

Updated Equipment and Crafting Overhaul (ECO).  
Updated xEdit.  
Updated Mod Organizer 2.  
Updated M8r's Complex Sorter.  
Updated exported MCM settings.  

Added Jampads 2 - a Sim Settlements 2 Add-on.  
Added Sim Settlements 2 - Junk Town 2 Addon Pack.  
Added Sim Settlements 2 - Apocalyptic Additions Addon Pack.  
Added Sim Settlements 2 - So I Made Plans Addon Pack.  
Added SimHomestead 2 - A SimSettlements 2 addon.  
Added SS2 Addon - Bare Essentials.  
Added Vault-Tec Tools - Sim Settlements 2 Addon Pack.  
Added Sim Settlements 2 - Junk Town - FENCES 2 Addon Pack.  
Added Sim Settlements 2 - Ruined Homes and Gardens 2.0.  
Added IDEK's Logistics Station 2.  
Added Sim Settlements 2 - Tech Settlements.  
Added Favelabulous.  
Added SS2 Blood Moon Raiders - A Sim Settlements 2 Addon Pack.  
Added Sim Settlements 2 - Rags and Riches.  
Added SS2 Radiant Municipal Power.  
Added Faster Upfront Settler Training SS2.  
Added Abernathy Farm - The Roof Diner.  
Added BOS Airport (Boston Airport) - Sim Settlements 2 - City Plan Contest - March 2022.  
Added Bunker Hill Mega City (Winner sim settlement 2 City plan conquest 2021-09).  
Added Bunker Hill Skymall - Sim Settlements 2 City Plan - City Plan Contest Entry September 2021.  
Added Castle Restoration Project - March City Plan Contest Entry.  
Added Choochoo1's Vault 88 Metro City Plan - October2021 Entry.  
Added Coastal Cottage - Sim Settlements 2 City Plan Contest Entry - July 2021.  
Added Cozy Covenant - Sim Settlements 2 City Plan Contest Finalist September 2021.  
Added Dugout Liquors (Croup Manor) - Sim Settlements 2 City Plan.  
Added Experimental Farm 06 (Coastal Cottage) - Sim Settlements 2 City Plan - July 2021 Contest Entry.  
Added Finch Farm The Arms Fair (Sim Settlement 2 City plan conquest 2022-02).  
Added Finch Salvage Recovery - Sim Settlements 2 City Plan Contest Winner February 2022.  
Added Fort Somerville (Somerville Place) - Sim Settlements 2 City Plan.  
Added Fort Tenpines Sim Settlements 2 City plan entry for July2021.  
Added Greentop Cannery Sim Settlements 2 City Plan.  
Added Hang'em Mall (Hangman's Alley) - Sim Settlements 2 City Plan.  
Added Karvocs Kollections.  
Added Kingsport Lighthouse City Plan SS2 Contest Entry April 2021.  
Added Longfellow's Floating Islands - City Plan SS2 Contest Winner June 2021.  
Added Minutemen and Manor - Sim Settlements 2 - City Plan Contest Finalist - March 2021.  
Added Minutemen Castle Command - Sim Settlements 2 City Plan Contest March 2022.  
Added Murkburgers (Murkwater Construction) - Sim Settlements 2 City Plan.  
Added Murkwater City Plan Entry for May 2021 All praise Atom for it is right to do so.  
Added Murkwater Observatory (Finalist sim settlement 2 City plan conquest 2021-05).  
Added National Park Prison - Sim Settlements 2 City Plan.  
Added Nordhagen Fishery - Sim Settlements 2 City Plan Contest April 2022.  
Added Oberland Outpost - Sim Settlements 2 City Plan Contest Entry November 2021.  
Added Oberland Station - The Scavengers' Paradise (Sim Settlement 2 City plan conquest 2021-11).  
Added Oberland Station Planet X - SS2 November City Plan Contest.  
Added Port Dalton SS2 April 2022 City Plan Contest entry.  
Added Red Rocket Foundry - Sim Settlements 2 City Plan Contest Entry - March 2021.  
Added Red Rocket Happy City (Sim Settlements 2 City Plan Contest 2021-03).  
Added Red Rocket Reclamation.  
Added Reina's Croup Market - City Plan Contest Entry March 2021.  
Added Reina's Vault 88 City Plan for Sim Settlements 2.  
Added Sanctuary City Plan SS2 Contest Entry June 2021.  
Added Sim Settlements 2 - Blackbelt's Vault 88.  
Added Sim Settlements 2 - Captain Croup Bar and Dive Entry for the City Plan Contest for March 2021.  
Added Sim Settlements 2 - Murkwater Industries.  
Added Sim Settlements 2 - Rad Scrappers Marina August 2021 Contest Entry.  
Added Sim Settlements 2 - Spectacle Prison.  
Added Sim Settlements 2 - The National Park Training Ground.  
Added Sim Settlements 2 City Plan Croup Manor - CroumanVil.  
Added Sim Settlements 2 City Plan Echo Lake Lumber - EchoVil.  
Added Sim Settlements 2 City Plan Kingsport Lighthouse - KingsVil.  
Added Sim Settlements 2 City Plan Murkwater Construction Site - DozerVil.  
Added Simple Sanctuary - Sim Settlements 2 City Plan.  
Added Slog Tarberries and Fitness - Sim Settlements 2 City Plan - August 2021 Contest Entry.  
Added Somerville Pet Place - Sim Settlements 2 City Plan Contest Entry November 2021.  
Added Somerville Place (Sim Settlement 2 City plan contest entry 2021-11).  
Added SS2 City Plan - Coastal Cottage Nuka-Cade Vacation Destination.  
Added SS2 Nordhagen Beach Seaside Views - City Plan Contest April 2022.  
Added SS2 Sanctuary Green Hills.  
Added Starlight Hive - Sim Settlements 2 City Plan.  
Added Sunshine Hive (Sunshine Tidings Co-Op) - Sim Settlements 2 City Plan.  
Added Sunshine Tiding - The medical center (Winner Sim Settlement 2 City plan conquest 2022-01).  
Added Tenpines Bluff a fortified Village.  
Added Tenpines Hive - Sim Settlements 2 City Plan.  
Added The Alley Cabaret a Sim Settlements 2 City Plan Contest Finalist - April 2021.  
Added The Castle Rebuilt-Minutemen HQ - Sim Settlements 2 City Plan and Layouts-Blueprints.  
Added The Circle (Red Rocket) - Sim Settlements 2 City Plan Contest Entry - March 2021 - Winner.  
Added The Croup SS2 Contest Plan Mar 21.  
Added The Slog An ingenious pool(Sim Settlements 2 City Plan Contest 2021-08).  
Added Vaulted Vault 88 - Sim Settlements 2 City Plan Contest Winner October 2021.  
Added Zimonja Cavern - Sim Settlements 2 City Plan Contest Winner July 2021.  
Added SS2 City Plan Pack - ZJ PerfPlans.  
Added SS2 - Vit-O-Matic Sensors for West Tek Tactical Optics.  

Removed Build Your Own Pool.  
Removed Advanced AI Tweaks.  
Removed Sleepless Nights.  
Removed Real Troughs - New Brahmin Feeders.  
Removed The Kuro Tab.  
Removed Vertibird Landing Pad.  
Removed Shaw Memorial Restoration.  
Removed Sim Settlements 2 XDI Perk Speech Check patch.  

Where There's Smoke should no longer have frozen dialogue scenes.  
Changed name of Engineering Workbench to Power Armor Workbench.  
Fixed gold crafting costs at the Junk Workbench (probably).  
Unpacked Auto Hack.  
Unpacked Auto Lockpick.  
Unpacked Improved Disarm.  
Unpacked Legendary Radroach Fix.  
Unpacked Rusty Face Fix.  
Unpacked Weapon Quickswap.  
Unpacked Creation Club Delayed.  
Unpacked Automatically Lowered Weapons.  
Unpacked BS Defence.  
Unpacked Fortune Finder 4 Fix - Enhanced Bottlecap Mine.  

Known issues:  

Raider Armor isn't tagged.  
Dreadnaught armor isn't tagged.  
A few other things from Raider Overhaul aren't tagged.  
Some CC content isn't tagged (CC profile only).  
Taffington Boathouse has collision issues.  
One house at the top of the hill in Concord is invisible, causing culling issues.  
Presets have default hair.  
Claudia (12047d77, 12047d55) spawns naked.  
Heather Casdin and Vault 494 use the same radio frequency.  
One Synth helmet is double tagged.  

---

2022/05/05

Version 6.0.0 Beta 2

Updated Sim Settlements 2.  
Updated Sim Settlements 2 - Chapter 2.  
Updated Workshop Framework.  
Updated Equipment and Crafting Overhaul (ECO).  
Updated This is Trash.  
Updated Heather Casdin.  
Updated 4estGimp - Raider Overhaul ONE.  
Updated Fallout 4 Ultimate Window Overhaul.  
Updated Wetness Shader Fix.  
Updated Subversion.  
Updated NPC Level Scaling Patch.  
Updated Fast Start - Skip Prewar Sanctuary.  
Updated Pra's Random Addon for SS2.  
Updated Power Combined Arms.  
Updated Nuka World Plus.  
Updated Creative Perks Plus.  
Updated Companion Thoughts Overhaul.  

Added SS2 Addon - Unlock Vanilla Recruitable Vendors.  
Added Nuka Cola and Beverage Fix.  
Added Inside Jobs Small Fixes.  
Added Discord Rich Presence.  
Added Random Valuables Redux.  
Added I'm Darlene.  
Added Old Time Religion.  
Added SS2 XDI Perk Speech Check.  

Removed Recruitable NPCs.  
Removed Animal Rescue.  
Removed NPC Level Scaling - Beastly Bosses plugin.  

Fixed TCD Skin Overlays.  
Re-enabled Crosshair (I think? Did I replace my old one with it? If not, let me know, I'll export it again).  
Created new MCM Settings Manager output.  
Reran sorter plugins.  

Notes:
This is Trash breaks a lot of cells. I only made the plugin at this stage, I didn't do any cell regeneration.  
I have not yet used Old Time Religion or I'm Darlene, so I have no idea if there are any issues. Happy to hear about anything you encounter.  

---

2022/04/07

Version 6.0.0 Beta 1

Updated Sim Settlements 2.  
Updated Sim Settlements 2 - Chapter 2.  
Updated 4estGimp Super Mutant Redux.  
Updated Equipment and Crafting Overhaul (ECO).  
Updated Workshop Framework.  
Updated We Are The Minutemen.  
Updated Wattz Laser Gun - Unofficial Update.  
Updated Recruitable NPCs.  
Updated Nuka World Plus.  
Updated Kat's Power Armor Repair Kits.  
Updated Creative Perks Plus.  
Updated Combined Arms Integration Project.  
Updated Better Companions - All in One.  
Updated 4estGimp - Raider Overhaul One.  
Added Bobblehead Randomizer.  
Added Hot Rodder Hazmat Suit.  
Added NPC Level Scaling.  
Added SS2 - Pra's Random Addon.  
Added Sim Settlements 2 Scrappers.  
Added NPC Scaling.  
Added Advanced AI Tweaks.  
Added Animal Rescue.  
Added 4estGimp Wattz Laser Rifle ini.  
Added 4estGimp W.A.T.M. ini.  
Added Synth Overhaul C.A.S.T. Immersive Naming.  
Added Who's The General - Minuteman Quest Cleanup.  
Added We Are The Minutemen - Enhanced Textures.  
Added Underwater Glass Fix.  
Added Subversion - The Institute-Railroad Alliance Alternative.  
Added Smart Recruitment Radio Beacon.  
Added Fast Start - Skip Prewar Sanctuary.  
Removed 10mm Pistol - Stahl Arms STA-20.  
Removed Multiple Floor Sandboxing.  
Removed Start Me Up.  
Removed The Danse Dilemma.  
Removed Spare Railroad as Institute.  
Removed Leveled Raiders.  
Removed Total's Leveled Raider Overhaul.  
Archimedes-II can no longer be crafted. Ammo can only be crafted for it once the player has entered the Institute.  
Better patches for consistency with ECO's Legendary OMODs.  
Fixed an issue with Unique Unique's Silver Submachine Gun (OMOD was accidentally overwritten by Legendary Swap).  
Forwarded grammatical fixes from UFO4P into Better Notes and Publick Occurrences Expanded.  
Changed Minuteman General's default outfit to Strategist Duster.  
Changed Pickman's default outfit to Survivalist Outfit.  
Changed Synth Boss Outfits to a mixture of lists from Synth Overhaul and Mercenary.  
Changed dead Minuteman's outfit to a less powerful list of items.  
Changed Phyllis Daily's outfit to WF Alice Long Coat.  
Changed capitalization of WF Alice Long Coat because it bothered me.  
New patch for UFO4P and Creation Club content.  
New patch for ECO and BoS Overhaul.  
New patch for ECO and Synth Overhaul.  
New patch for Super Mutant Redux stuff.  
New patch for NPC Scaling stuff.  
New patch for SS2 Robot Mod and Live Action Handy.  
Numerous load order adjustments.  
Removed Combined Arms unique ammo types from Scrounger since they are no longer used.  
Many edits to Lively's Tweaks and CustomLLs.  
And about a thousand other tiny changes that I forgot and/or didn't document properly.

---

2022/03/15

Version 5.2.1

Added SS2C2 - 3DNPC Patch.  
Updated Sim Settlements 2.  
Updated SS2 - Chapter 2.  
Updated Workshop Framework.  
Updated Combined Arms Integration Project.  
Fixed various issues with Combined Arms Integration Project and Creative Perks Plus not playing nice together.  
Fixed and added some presets.  
Fixed an issue with TCD Overlays causing a black face bug on the player character.  
Fixed an issue with Wattz guns spawning in an unplayable state.

---

2022/03/07

Version 5.2.0

Added More Active AI.  
Added Power Armor to the People.  
Added Immersive Candles.  
Added 10mm Pistol Modification Pack.  
Added .44 Magnum Modification Pack.  
Added Deliverer Modification Pack.  
Added Institute Receivers Plus.  
Added Wattz Laser Gun - Unofficial Update.  
Added Provisioner and Supply Line Management System.  
Added SS2 - Pra's Random Addon.  
Added Super Mutant Weaponry - Post-Apocalyptic Weapons.  
Added Automatron Randomized Bots.  
Added Nomads SPECIAL Replacer.  
Added Combined Arms Integration Project.  
Added Power Combined Arms.  
Added Armored Nuka World.  
Added Settlers Go Shopping.  
Added Recruitable NPCs.  
Updated Sim Settlements 2.  
Updated SS2 - Chapter 2.  
Updated SS2 - Nobody's Leaders 2.  
Updated See Through Scopes.  
Updated See Through Scopes - MCM Menu.  
Updated Workshop Plus.  
Updated Workshop Framework.  
Updated Creative Perks Plus.  
Updated Kat & Lively Gettin Down. Loooots of perk edits and bug fixes.  
Updated Standalone Workbenches.  
Updated Tattoos Collection by Dreivor Overlays Edition.  
Removed Modcols for Weapons Mod.  
Removed Beantown Interiors and all related patches/files/configs.  
Removed Underground Hideout Redux Player Home.  
Removed SS2 Extended.  
Removed More Power Armor Display Stations.  
Removed Immersive Hub City Auto Wreckers.  
Added a new loading screen referencing the need for Demolition Expert to disarm traps.  
Cleaned up the downloads folder a little bit.  
Nerfed the BGL-3 a bit.  
Changed some stuff around in CustomLLs and Lively's Tweaks.  
Updated some Crafting patches.  
Removed most ROTC plans.  
Probably a few dozen other micro changes I don't remember. Sorry.

---

2022/02/03

Version 5.1.0

Added a crafting patch for Power Armor Airdrop.  
Added Improved Disarm - Auto Lockpick Consistency.  
Added User Submitted Presets.  
Added Sim Settlements 2 Automatron Mod.  
Added SS2 Nobody's Leaders.  
Added H.A.R.D.Core - Fusion Generator Overhaul.  
Added Modcols for Weapons Mod.  
Added Shaw Memorial Restoration.  
Added Flicker Fixer ESL v5.7  
Added More Feral Ghouls Priest Allen Fix.  
Added NX Encounter Zones.  
Added Settlement Attack Spawns Outside the Settlement - Alpha.  
Added Fallout 4 - Hot Coffee.  
Added Immersive Covenant Compound.  
Added CC Morgan's Space Suit - ECO Style (CC Profile only).  
Added Various Backpack Fixes - 1st Person Crouch.  
Added Magazine Rack Extended.  
Added Magazine Rack Extended - Fourville.  
Added NCR Veteran Ranger - F4NV.  
Added SS2C2 Shroud Manor Patch.  
Updated the damn ECO patches to use the new damn mod page because they keep getting moved and deleted and I'm starting to get kind of pissy about it.  
Updated Sim Settlements 2.  
Updated SS2 Chapter 2.  
Updated Ransacked Relays and Shuddersome Subways.  
Updated Gunner Outfit Pack (STANDALONE).  
Updated Ownership Fixes.  
Updated Combined Arms Expansion Pack.  
Updated Creative Perks Plus. This has no effect on Opus' perk chart.  
Removed Quick Reflexes.  
Removed Carbon Fiber Metal Armor.  
Removed Leaders and Legends of the New Commonwealth.  
Removed NCR Ranger Veteran Armor.  
Removed NCR Ranger Veteran Riot Helmet CTD Fix.  
Removed Gunner Outfit Pack - Leveled List Integration and Outfit Patch  
Removed Gunner Outfit Pack - PA Repair Kits Patch.  
Removed Subways of the Commonwealth.  
Updated Lively's Tweaks to include a super duper tiny micro patch between Hardcore Fusion thingy and Ownership Fixes.  
Removed a bunch of old/junk data from Lively's Tweaks.esp.  
Minor bug fix to Explorer rank 4.  
Removed Universal Workbench chem from the Utility Workbench.  
Fixed a typo in Institute Story.  
Removed a record from Interiors Enhanced that conflicted with Officer's Revolver.  
Made Super Mutant armor unequippable by the player (probably).  
Added some user-submitted presets.

---

2022/01/18

Version 5.0.5

Removed additional useless leftover archives from my downloads folder that got sucked into the compile. Sorry about that! You should all be able to install the list without any issues now (I hope).

---

2022/01/17

Version 5.0.4

Disabled one more tree from Another Pine Tree Mod.  
Fixed a typo in a RU556 OMOD record.  
Fixed outfit record used by various NPCs such as Roger Warwick, Randy, and some traveling visitors.  
Fixed outfit record for Winlock.  
Renamed settings holotape for See Through Scopes.  
Robot Repair Kits can no longer be crafted until the Mechanical Menace quest is completed.  
Removed the oil can suppressors from Combined Arms because I think they look silly.  
- Note that only the cobjs have been removed, so if you have weapons in your game with this already attached, your game is still perfectly fine to continue playing.  
Renamed PL-15 Lebedev and MP443 Grach to get rid of the quotes around the names.  
Made a patch so Gunner Outfit Pack Leveled List Injection Power Armors get repaired by Kat's Power Armor Repair Kits.  
Edited Conditions on a few dozen loading screens.  
Fixed another crash in Xander's Aid because lodgen hates me.

---

2022/01/14

Version 5.0.3

Drastically reduced loot obtained from This is Trash.  
Fixed some leftover errors in Lively's Tweaks.  
Updated Creative Perks Plus. Most notably for us, this expands the Explorer perk.  
Fixed consistent crash due to corrupted texture files in Kelly Manor and Xander's Aid worldspaces. 100% my fault.

---

2022/01/11

Version 5.0.2

Fixed Crafting-CombinedArms.esp's Level requirements.  
Fixed Special stat scaling on Rifleman perk.  
Edited Terminal entry about Sanctuary in the Magnum Opus Beginner's Guide for clarity.  
Disabled 12 trees from Another Pine Forest that were clipping with Minuteman Watchtowers.  
Fixed Bullet to the Knee rank 1 requiring the player to be level 8 (should be 0, not sure how I managed to do that accidentally...).  
Edited Demolition Expert perk descriptions to account for disarming traps.

---

2022/01/09

Version 5.0.1

Fixed Kriss Vector crash.  
Fixed Wattz Terminal via deleting the terminal. Yep. That's how I roll.  
Fixed settlers spawning without clothing maybe? More testing needed.  
Fixed This is Trash not getting rid of a bunch of shit in Sanctuary.  
- Note: this update will respawn the trash can in every settlement.  
Updated CustomLLs.esp.  
Slight mod order and load order adjustments in non-CC profile.  
- These are easy for me to overlook from time to time since all of my testing is done in the CC profile, my apologies.  
Fixed the Chemistry Station, re: tons of dumbass stuff that shouldn't have been in there.

---

2022/01/08

Version 5.0.0

Added 4estGimp - Standalone Construction PA INNR.  
Added 4estGimp - CROSS_CourserStrigidae_CS_ini_ECO.  
Added 4estGimp - CROSS_COA_ini_ECO.  
Added 4estGimp - CROSS_BrotherhoodRecon_CS_ini_ECO.  
Added Abandoned Tunnels - Standalone Workbench Setup.  
Added Agency Arms Benelli M2 Shotgun.  
Added Another Pine Forest Mod.  
Added Baka ScrapHeap.  
Added BS Defence.  
Added Combined Arms - Expansion Pack.  
Added Cross Jetpack Crafting Highlight Fix.  
Added DLC Timing UFO4P Patch.  
Added Equipment and Crafting Overhaul (ECO).  
Added ECO Patches for:  
- Cross Brotherhood Recon
- Cross Chosen of Atom
- Cross Courser Strigidae
- Eli's Armour Compendium
- Fourville
- We Are The Minutemen
- Far West Minutemen
- Raider Overhaul
- Super Mutant Redux  
Added ECO Expansion - Legendary Modification Enhanced.  
Added ECO Expansion - Mythic Legendary Modifications.  
Added Legendary Modifications Enhanced.  
Added Legendary Radroach Fix.  
Added Legendary Swap with Reasonable Restrictions.  
- Added seven new patches for Legendary Swap (so far)...  
Added Grass Reworked.  
Added Gunner Outfit Pack - Lively's Crafting Tweaks.  
Added I've Got Wood - A Sanctuary Texture Overhaul.  
Added Improved Disarm.  
Added MCM Settings Manager.  
Added MMP4APA - Minuteman Paint for ALL Power Armors.  
Added NPCs Travel - MCM Settings Menu.  
Added Ownership Fixes.  
Added Portable Junk Recycler Mk 2.  
Added Quantum Creatures.  
Added Quick Reflexes - Slow Motion Favorites Menu.  
Added RoNin1971's UHD Landscape Environment.  
Added Settlement Tidy Bot.  
Added Sim Settlements 2: Chapter 2.  
Added Tales From the Commonwealth - Typo Patch.  
Added The Beantown Interiors Project - Precombined Visibility Patches.  
Added True Grass.  
Added Varied Gunner Mercenaries.  
Added W.A.T.M. - Power Armor Expansion.  
Added We Are The MInutemen - Tweaks - Fixes - Power Armor Expansion - Patches.  
Added You and What Army - More Minutemen Patrols.  
Updated 4estGimp M8r Complex Item Sorter Enhancements.  
Updated Abandoned Hub - Underground Railroad ReRedux.  
Updated Creative Perks Plus.  
Updated Inside Jobs.  
Updated Kat & Lively Gettin Down.  
Updated Kat's Power Armor Repair Kits.  
Updated Lively's Keywords Resource.  
Updated Lively's Tweaks.  
Updated M8r98a4f2's Complex Sorter.  
Updated Patches for Lively's Keywords Resource and Whisper's Workbenches.  
Updated Sim Settlements 2.  
Updated SS2 - Superstructures.  
Updated SS2 - Tiny Living.  
Updated SS2-XDI Compatibility Patch.  
Updated Workshop Framework.  
Removed 4estGimp - CROSS_BrotherhoodRecon_INNR_ini_CS1.9.  
Removed 4estGimp - CROSS_CourserStrigidae_INNR_ini_CS1.9.  
Removed 4estGimp - CROSS_CoA_INNR_ini_CS1.9.  
Removed Anom's Sanctuary Overhaul.  
Removed Armor and Clothing Overhaul (ACO).  
Removed Boston Natural Surroundings.  
Removed Crafting Mastery.  
Removed Free the Beards.  
Removed G2M Workshop.  
Removed Immersive and Extended Lexington.  
Removed Immersive and Extended Nahant.  
Removed Legendary Modification Enhanced.  
Removed Pine Trees Redone.  
Removed Portable Junk Recycler.  
Removed Road Flares.  
Removed Simple Clothing Keywords.  
Removed Simply Lowered Drawbridges.  
Removed Subway Runner.  
Removed Tomacuzi.  
Removed Useful Technical Documents - Legendaries.  
Removed Underground Redux - Whisper's Workbenches.  
Edited Four Leaf Clover rank 1 to only apply to body shots in VATS.  
Edited Four Leaf Clover rank 4 to properly apply to head shots.  
Edited description for Sniper rank 3.  
Reran sorter scripts and condensed sorter outputs to a single plugin per profile.  
Disabled Memory Manager patch in Buffout.  
There are so many other little changes but I stopped documenting them because it's SO MUCH. Sorry.

---

2021/11/16

Version 4.11.3

Updated Gunner Leveled Lists.

---

2021/11/15

Version 4.11.2

Reverted Gunner Outfit Pack Standalone to v3.0 for now.  
Reran sorter output 2 for both profiles.  
Removed Empty tag from empty containers.  
Adjusted CustomLLs a bit to address a handful of errors.

---

2021/11/13

Version 4.11.1

Updated Gunner Outfit Pack.  
Added TypicallySean's Perk Chart Alignment Fix.

---

2021/11/11

Version 4.11.0

Removed Fallon's Basement Overhaul.  
Removed Vicky's Duggout Inn.  
Removed An Office Fit For A Mayor.  
Minor load order adjustments.  
Reran sort output (part 1 only) for both profiles.

---

2021/11/11

Version 4.10.1

Hotfix for Kat & Lively Gettin Down.esp.

---

2021/11/10

Version 4.10.0

Added BCR - Hunting Shotgun Patch.  
Updated Creative Perks Plus.  
Added Beast351x's Creation Club Solar Cannon.  
Added Beast351x's Prototype Gauss Rifle.  
Added Power Armor Night Vision.  
Added CROSS Cryolance Uses Cryo Cells.  
Added Barber and Surgery - Front and Back Camera.  
Added AWARHERO - The Great Green Jewel.  
Handful of other smaller fixes and patches not worth mentioning.

---

2021/10/06

Version 4.9.1

Fixed electronics workbench placement in Abandoned Tunnels.  
Moved Castle Manhole exterior placement for Abandoned Tunnels.  
Cleaned up Vault Tec Property Storage cell.  
Fixed door issue in National Guard Bunker cell.  
Removed Nukatron from Abandoned Tunnels.  
Changed Franklin's default outfit to the Spacesuit Costume & Helmet.  
Removed Gunner Trunk from GNN.  
Disabled placement for Wasteland Survival Guide 05.  
Disabled placement for Live & Love 03.  
Edited Live & Love 03 to give +200 companion carry weight instead of +10.  
Replaced Wasteland Survival Guide 05 with Live & Love 03.  
Removed Minutemen Specialist Backpack refereneces. (Note: Did not delete the backpack outright so your saves will still be intact)  
We Are The Minutemen no longer forces a 96 hour waiting period between Minutemen Radiant Quests.  
Recategorized cooking cobj keywords from Manwell Rifle (CC Profile only).  
Fixed All Natural effects not applying properly.  
Fixed Cap Collector effects not applying properly.  
Disabled another tree from BNS.  
Fixed a few Fourville typos.  
Fixed some 3DNPCs typos.  
Fixed some more David Hunter typos.  
Edited Autohack's entry point to replace default because I keep accidentally opening the manual hack menu instead of autohacking and it annoyed me.  
Changed Lockpicking Rank 4 to unbreakable lockpicks.  
Updated Whisper's Extra Pieces and Snaps.

---

2021/09/22

Version 4.9.0

Added Armor and Clothing Overhaul.  
Added The Bleachers - A Diamond City Story.  
Added Castle in the Sky.  
Added Abandoned Hub - Underground Railroad Redux.  
Added Brotherhood Power Armor Drop Team.  
Updated SS2 Superstructures.  
Updated Creative Perks Plus.  
Edited Fourville's Too Many Cooks quest to clarify when/if it will fail in the crime scene stage.  
Reran sorter outputs for both profiles.  
Changed source download location for More Feral Ghouls.  
Fixed perk description for Rifleman Rank 1.  
A bunch of other minor little things that I don't recall off the top of my head because I'm bad at writing things down as I go.

---

2021/09/15

Version 4.8.8

Actually added Human Grab Attacks and Far Harbor Melee Killmove Frequency Rebalance this time. Sorry.  
Updated Kat & Lively Gettin Down (fixes a few weapons freezing at the workbench, like the Western Revolver, Personal Minigun, Heavy Incinerator, and Venom Gun, I think).  
Fixed David Hunter not giving you the first quest.  
Updated Load Order Library because I'm bad at keeping up with that.

---

2021/09/12

Version 4.8.7

Updated Buffout 4.  
Added new condition to David Hunter quest Hunting for Hunter.  
Fixed some zfighting in Lexington with four structures.  
Removed one OMOD from Kriss Vector.  
Fixed a few typos in Widow Shotgun.  
Added Expert lock to Widow Shotgun's hatch door.  
Fixed a typo in Explorer rank 1.  
Added GetQuestCompleted condition to Railroad Stealth Boy cobj.  
Moved Heather's Locator Signal from the Chem Bench to the Utility Bench.  
Fixed issue with M82A1 Magazine freezing the game at a Weapons Workbench.  
Changed category for M82A1 crafting from PISTOLS to SNIPER RIFLES. Little oversight there...  
Added Console Util. Note: this does nothing right now but I want to play around with it later.  
Added Human Grab Attacks.  
Added Far Harbor Melee Killmove Frequency Rebalance.

---

2021/09/07

Version 4.8.6

Fixed typo in Far West Minutemen.  
Removed Heavy Gunner Buffs Minigun Separately.  
Updated Buffout 4.  
Updated Kat's Power Armor Repair Kits for both profiles.  
Added Beantown Interiors - Typo Fixes and Optional Gnome Removal.  
Updated inis to probably fix camera issues and blood spatter on screen.

--

2021/09/05

Version 4.8.6

Removed Lively's Quest Tags.  
Removed Lively's Quest Tags - CC Edition.

---

2021/09/05

Version 4.8.5

Added Combined Arms ammo types to Scrounger's leveled lists.  
Updated Buffout 4.  
Updated Whisper's Extra Pieces & Snaps.  
Updated CustomLLs.  
Updated Lively's Tweaks.  
Bug fix for Action Girl rank 3.  
Bug fix in Luck rank 2 - Lone Wanderer will now properly display in perk chart.  
Bug fix for Black Widow rank 3.  
Bug fix for Classic Criticals rank 2.  
Edited Beginner's Luck level requirements.  
Bug fix for Grim Reaper's Sprint/Deadly Strike.  
Edited all ranks of Gunslinger.  
Edited all ranks of Heavy Gunner.  
Bug fix for previs in General Atomics Factory interior.  
Renamed Ammo Disassembly to Ammo Breakdown.  
Moved Ammo Breakdown category to the top of the Ammunition Workbench.

---

2021/08/28

Version 4.8.4

Updated Mod Organizer 2.  
Updated 4estGimp - Far West Minutemen - No Cybernetics - No AWKCR.  
Updated DLC Timing.  
Updated 4estGimp Raider Overhaul ONE.  
Updated 4estGimp Complex Item Sorter Enhancements.  
Updated Sanctuary Hills Overhaul.  
Updated 4estGimp Hellfire X-03 INNR.  
Updated Creative Perks Plus.  
Updated Crafting-Raider Overhaul patch.  
Removed Night Vision from Night Person Rank 3.  
Removed Faster Terminal Displays (replaced in Lively's Tweaks).  
Removed Rain of Brass (replaced in Lively's Tweaks).  
Removed Longer Power Lines (replaced in Lively's Tweaks).  
Lots of GMST changes in Lively's Tweaks.  
Reran sorting outputs for both profiles.

---

2021/08/11

Version 4.8.3

Updated Sim Settlements 2.  
Updated Workshop Framework.  
Updated Baka Wait Anywhere.  
Removed Nuclear Weathers.  
Updated readme and image links for the gallery and website.  
Probably something else I don't remember.

--

2021/08/05

Version 4.8.2

Updated Kat's Power Armor Repair Kits.  
Updated Lively's Quest Tags. Added new tags for around 40 quests or so that I missed previously.  
Removed 4est-lively-quest-tags.esp. Became redundant and just kind of in the way.  
Removed one tree from Boston Natural Surroundings that was growing through Minutemen Watchtower India.  
Fixed an issue where X-01 and T-60 Repair Kits couldn't be crafted at the Engineering Workbench.

---

2021/07/30

Version 4.8.1

Added Kat's Power Armor Repair Kits.  
Added Underground Hideout Redux Player Home.  
Updated some quest tag icons.  
Updated Lively's Tweaks. More specifically, added more terminal entries, and added a Holotape copy of the entries to the terminal. Now you can read it on the go!  
Reran sorter outputs.  
Updated stuff on LoadOrderLibrary.

---

2021/07/28

Version 4.8.0

Added Rutah Tattoo Pack for LooksMenu.  
Added Tattoos Collection by Dreivor - Overlays Edition.  
Added KS Hairdos - Addon(s) with Physics.  
Added 4estGimp - Excavator PA INNR.  
Updated Vault 88 Essentials.  
Removed Raider Gangs Extended Fixed & Cleaned.  
Removed ENB binaries.  
Removed gnomes from Beantown Interiors Project.  
Reran sorter outputs.

---

2021/07/27

Version 4.7.0

Removed Pack Attack NPC Edition.  
Removed Pack Attack Companion Edition.  
Removed More Realistic Cats.

---

2021/07/20

Version 4.6.0

Added Blink Grenades.  
Added CROSS Jetpacks.  
Added CROSS Recall Collar.  
Added Portable Junk Recycler.  
Added Unique Uniques.  
Added DNX Body Tattoos.  
Added Rad-Ban Eyewear Inc.  
Added Legendary Modification Enhanced.  
Added Clean Homemaker Greenhouses.  
Added Nuclear Weather.  
Added Cobra - Officer's Revolver.  
Added Evil Institute HD.  
Added Follower Stealth Distance Fix.  
Added 4estGimp - CROSS Armor INNR and .ini for M8r's Complex Sorter.  
Added 4estGimp - CROSS Weapon INNR and .ini for M8r's Complex Sorter.  
Updated DLC Timing.  
Updated Publick Occurrences Expanded.  
Updated Bullet Counted Reload System.  
Updated Creative Perks Plus.  
Updated M8r's Complex Sorter.  
Updated 4estGimp - M8r98a4f2's Complex Item Sorter Enhancements.  
Removed IceStorm's MK23 Socom.  
Reran sorter outputs. A lot.

---

2021/07/09

Version 4.5.4

Added the Magnum Opus Beginner's Guide and associated quest.  
Added about a dozen new loading screens to help players understand the mods better, and occasionally give subtle (or not so subtle) hints on how to find various interesting locations and quests.  
Added DLC Timing.  
Updated Sim Settlements 2.  
Updated M8r Complex Sorter.  
Updated all of 4estGimp's mods.  
Updated Sorter outputs.  
Updated Readme's MCM Settings.  
Updated Readme's FAQ section.  
Updated Crafting-WestTek patch.  
Updated Crafting-MiscUtil patch.  
Updated Lively's Tweaks.  
Updated Lively's Quest Tags.  
Player will no longer say "Call me Charmer" or "Meow" when proccing Beginner's Luck.  
Edited Gumshoe Rank 2 Perk conditions.  
Increased maximum number of possible concurrent Minutemen quests from 1 to 2.

---

2021/07/03

Version 4.5.3

Removed Vault 81 Molerat Disease Fix.

---

2021/07/03

Version 4.5.2

Removed More Attackers Get Off My Build Zone.  
Removed Swinging Animated Meat Bags.

---

2021/07/02

Version 4.5.1

Removed Complex Vendors.

---

2021/07/02

Version 4.5.0

Removed CWSS Redux.  
Removed SS2 Traveling Visitors.  
Updated sorting outputs accordingly.

---

2021/07/01

Version 4.4.0

Removed Malevolent Ellen Overhaul.  
Added Wasteland Heroines Replacer - Ellen the cartographer.  
Updated Sim Settlements 2.  
Fixed a typo in Cap Collector perk description.  
Fixed a typo in Ninja perk description.  
Added Vault 494 - A Vault-Tec Story.  
Added Hilda Hughes - An Institute Story.  
Updated David Hunter - A Brotherhood Story.  
Updated Combined Arms.  
Updated Consume Without Pickup.  
Changed Quest Icon tag for Saints & Sinners.  
Consistency patching for the various Silver Shroud outfits in the game. Think I got 'em all...  
Disabled Hunting Shotgun BCR patch (for now?) because I don't really know what's going on there and I'm kinda lazy.

---

2021/06/24

Version 4.3.0

Updated Creative Perks Plus.  
Updated Kat and Lively Gettin Down.  
Recompiled for Wabbajack build version 2.5.0.0.

---

2021/06/23

Version 4.2.6

Updated sorting patches to address missing masters issues for the CC Profile.  
Added FO4LODGen.  
Added NeuraLOD Resources.  
Added FO4LODGen Resources.  
Added Luxor's Far Harbor HQ Tree LOD.  
Added LODGen Output.

---

2021/06/23

Version 4.2.5

Moved a note from Lore Notes into a mailbox, as it was previously floating in the air near Codsworth.  
Disabled a floating soap dispenser. Again.  
Removed Respawn flag from a few fences in Sanctuary.  
Fixed Quest Tag Icons for Xander's Aid.  
Fixed Quest Tag Icon for Rock 'em Sock 'em Robots (3DNPCs quest).  
Fixed a typo in Inspirational Rank 2.  
Added Ellen the Cartographer.  
Added Malevolent Ellen.  
Removed MsRae's Commonwealth Interiors.  
Reverted ESL flag on QuickTrade Redux.  
Removed Webmetz's CC Sorting Patches.  
Reran all sorters to generate new outputs.  
Removed modular support for Creation Club content. This may change in the future, I need to think of a better way to do it.  
Updated ENB binaries.

---

2021/06/20

Version 4.2.4

Updated FallUI - Inventory.  
Updated FallUI - HUD.  
Updated Fallout Priority - f4se plugin.  
Removed Wait Anywhere.  
Added Baka Wait Anywhere.

---

2021/06/12

Version 4.2.3

Hotfix for Kat and Lively Gettin Down.esp. Perks on Perception 3 and 4 will now display and work properly.

---

2021/06/19

Version 4.2.2

Removed HUDMenuSet from executables in MO2.  
Changed Wasteland Survival Guide #05. Failed to actually test this because I forgot.  
Reverted ESL flag on Lively's Tweaks.esp.  
Reverted ESL flag on Lexington Previs.esp.  
Updated Whisper's Extra Pieces and Snaps.  
Updated Creative Perks Plus.  
Updated Kat and Lively Gettin Down.  
Added Crafting-PANPC.  
Added Crafting-SportyUnderwear.  
Added Lively's Quest Tags.  
Added Lively's Quest Tags - CC Edition (CC profile only).  
Added complex sorter patch for handmade shotgun. (CC profile only).  
Reduced base value of Uzi.  
Edited a note in Zetan Armory (CC profile only).  
Edited the names and descriptions of some OMODs for the Wattz Laser Rifle.  
Edited sorting tag for Emergency Flare.  
Edited quest stage 25 in The Ritual of Ug-Qualtoth from Far Harbor Story to accurately reflect where the player should craft Ug-Qualtoth's Blade.  
Moved some holotapes out of the Chemlab. Again. And again. And AGAIN AND AGAIN AND AGAIN IT NEVER ENDS.  
Added a fix for an issue with Subway Runner and Pint-Sized Slasher (CC profile only).  
Added an empty mod for users to dump their Workbase archives into without fear of updates deleting them.

---

2021/06/12

Version 4.2.1

Added equip slot 46 to Hard Hat.  
Disabled a tree in Sanctuary.  
Edited description for Local Leader rank 2.  
Fixed the Defense Gun (I think).  
Updated modlist build in accordance with Wabbajack's hotfix in regards to game data paths. Thanks bossman.

---

2021/06/12

Version 4.2.0

Added NUCLEAR Nude. The list is still NeverNude, don't worry. No I won't help you remove the NeverNude body. It's not that hard to figure out and I personally prefer NeverNude, so deal with it.  
Added Sporty Underwear.  
Updated Workshop Framework.  
Updated Sim Settlements 2.  
Updated Console Commands Extender.  
Updated Fallout Priority. I'll keep using this for a bit, but quite frankly, I haven't seen any difference myself so far.  
Updated M8r Complex Sorter output (both profiles).  
Removed CBBE Ida Body Texture.  
Removed Lacy Underwear.  
Fixed Cazador stuff. I accidentally broke the patch for it in the last update. C'est la vie.  
Fixed Explorer perk again. My bad.  
Fixed & updated readme MCM/holotape config instructions.

---

2021/06/10

Version 4.1.0

Reverted ESL flags from a few mods.  
Updated FallUI HUD.  
Updated Buffout 4.  
Updated Lively's HUD Preset. This will likely be an ongoing thing.  
Removed fast travel quest stage from Explorer Rank 1.  
Edited Explorer Rank 1 perk description.  
Removed fast travel quest stage from Explorer Rank 2.  
Merged Explorer Rank 2 and Explorer Rank 4.  
Edited Explorer Rank 2 perk description.  
Removed Explorer Ranks 3 and 4.  
Moved a light that was floating in the middle of the street in Concord.  
Added equip slot 46 - Headband to Minuteman Hat.  
Removed all globals, replicas, hardammo, terminal entries, mcm menus, and all related records from Crafting Mastery.  
Fixed a lot of shit in Sanctuary; broke a fence, moved a mailbox, fixed a bridge. You know, the usual.

---

2021/06/09

Version 4.0.1

Updated FallUI.  
Changed default FallUI font setting.

---

2021/06/09

Version 4.0.0

Fixed a lot of minor quest stuff caused by adding quest tag icons.  
Added support for some Creation Club Content. More details in Readme.  
Added Creation Club Delayed.  
Added Pack Attack NPC Edition.  
Added Pack Attack Companion Edition.  
Added Pack Attack SS2 patch.  
Added Fallout Priority - f4se plugin.  
Added Webmetz's Molotovless Raiders Extended.  
Added Total's Swinging Super Mutant Redux Meat Bags.  
Added Total's Leveled Raider Overhaul.  
Added Combined Arms - Modern Weapons Pack.  
Added PA Ownership Fix (with No PA Battery Pathing).  
Removed ROLL (this was Raider Overhaul Leveled Lists created by me; they have been mostly merged into the main file on Nexus).  
Added Protectron Subway Steward Fix.  
Edited subway travel & bed costs.  
Removed PL-14 'Lebredev'.  
Removed Steyr AUG A-1.  
Removed BerettaM9FS.  
Removed Heckler und Koch - G36 Complex.  
Removed HK G36 Complex Constructable Mods and Addons.  
Removed 9x39 Project.  
Removed Seventy Six Weathers.  
Removed Combined Weathers.  
Updated Lively's Tweaks.  
Updated Whisper's Extra Pieces and Snaps.  
Updated M8r Complex Sorter.  
Updated Methodology stuff.  
Updated BNS Adjusted.  
Updated Unofficial Fallout 4 Patch.  
Updated FallUI - Inventory.  
Compacted & ESL-flagged about 180 plugins.  
Made a ton of custom changes to the Creation Club stuff, so don't be surprised if it doesn't behave in the exact way you are expecting.

---

2021/05/29

Version 3.1.3

Added Vault 88 Essentials.  
Added FallUI - HUD.  
Rebuilt/tweaked Lively's HUD Preset to work with FallUI - HUD.  
Updated Sim Settlements 2.  
Updated Workshop Framework.  
Updated Workshop Plus.  
Updated Creative Perks Plus.  
Updated Kat and Lively Gettin Down. Loootttssss of consistency patching and fixes.  
Changed Heather's Bag from slot 46 (Left Arm Armor) to slot 55 (the proper slot for bags).  
Fixed two cobjs both referencing Big Leagues rank 5 (which no longer exists...).  
Removed Commando Buffs Submachine Gun Separately (my own tweaks are in the perk overhaul now).  
Removed Critical Hits Outside VATS.  
Removed Vault 88 - More Vault Rooms.  
Removed DEF UI.  
Removed HUDFramework DefUI Compatibility Patch.  
Removed SS2 Workshop HUD Override.  
Removed No Quest Autostart - BoS Fire Support.  
Removed No Quest Autostart - Automatron.  
Removed No Quest Autostart - Far Harbor.  
Removed No Quest Autostart - Nuka World.

---

2021/05/16

Version 3.1.2

Updated Sim Settlements 2.  
Updated Workshop Framework.  
Added NCR Ranger Veteran Riot Helmet CTD Fix.  
Updated Kat and Lively Gettin Down.

---

2021/05/12

Version 3.1.1

Fixed Sorter Output not downloading.

---

05/12/2021

Version 3.1.0

Added Creative Perks.  
Added Creative Perks Plus.  
Added Kat's tweaks to said perk mods.  
Updated readme.

---

2021/05/09

Version 3.0.7

Actually included the aforementioned Concord fixes from the 3.0.6 changelog.

---

2021/05/09

Version 3.0.6

Removed The Lost Vault.  
Removed three trees from Boston Natural Surroundings.  
Removed a kickball.  
Removed a pair of scissors.  
Rebuilt three cells in Concord.  
Some leveled list adjustments.  
Changed Ballistic Weave's requirements to possibly include vanilla conditions as well as the new conditions so please for the love of god stop asking me about ballistic weave.

---

2021/05/08

Version 3.0.5

Fixed issues with the non-existent Cybernetics Workbench. All items previously found there are now in either the Armorsmith, Ammunition, or Weaponsmith workbenches.  
Moved G2M Holotape to the Utility Workbench.

---

2021/05/08

Version 3.0.4

Fixed Complex Sorter output plugin.

---

2021/05/08

Version 3.0.3

Removed Synthetic Zombies.  
Added 4estGimp - Enclave X-02 PA INNR and ini for Complex Item Sorter.  
Added 4estGimp - Hellfire X-03 PA INNR and ini for Complex Item Sorter.  
Added Lively's Keyword Resource.  
Added 4estGimp - Enclave X-02 PA INNR and ini for Complex Item Sorter.  
Added 4estGimp - Hellfire X-03 PA INNR and ini for Complex Item Sorter.  
Removed cazador missiles from some sentry bots.  
Fixed that weird house with no collision in Lexington.

---

2021/05/05

Version 3.0.2

Updated 4estGimp - M8r98a4f2's Complex Item Sorter Enhancements.  
Updated 4estGimp - Raider Overhaul ONE - All Files - No AWKCR.  
Updated Better Sleep and Wait Menu.  
Updated 4estGimp - Super Mutant Redux-No AWKCR.  
Removed CROSS Pre-War Cybernetics.  
Removed Read Notes from Containers and Corpses.  
Removed Better Flares.  

---

2021/05/02

Version 3.0.1

Fixed Drumlin Diner.  
Fixed Sanctuary Root Cellar.  
Fixed Piper's Outfit.  
Fixed Power Armor sorting tags for modded PAs.  
Fixed sorting tags for Leather and Raider armors.  
Fix Red Rocket + This is Trash compatibility issue.

---

2021/05/01

Version 3.0.0

Rewrote readme in its entirety.  
Downgraded MO2. Sorry, I couldn't get profile-specific inis to work.  
Added The Lost Vault.  
Added Subways of the Commonwealth.  
Added Anom's Sanctuary Hills Overhaul.  
Added Root Cellar Shelter.  
Added Ransacked Relays and Shuddersome Subways.  
Added The Natural Bundle - Assorted Textures - Submarine Set 2K.  
Added The Natural Bundle - Assorted Textures - Cave Set 2K.  
Added The Natural Bundle - Assorted Textures - Masonry Set 2K.  
Added Commonwealth Wilderness Overhaul.  
Added MsRae's Commonwealth Interiors.  
Added 4est Gimp - FallUI Complex Item Sorter Enhancements.  
Added source download for Lively's Keyword Resource.  
Added source downloads for Patches for Lively's Keywords Resource and Whisper's Standalone Workbenches.  
Added 4estGimp - Raider Overhaul ONE - All Files - No AWKCR.  
Added Super Mutant Redux.  
Added 4estGimp - Super Mutant Redux - No AWKCR.  
Added 4estGimp - SuperMutantRedux_INNRsFallUI.  
Added Synth Overhaul - C.A.S.T.  
Added 4estGimp - Synth Overhaul INNR 4 FallUI and R88.  
Added True Storms.  
Added Vivid Weathers.  
Added Weather Synergy.  
Added Seventy-Six Weathers.  
Added Fallout 4 Enhanced Color Correction.  
Added Merged Weather Overhaul.  
Added We Are the Minutemen.  
Added Far West Minutemen.  
Added 4estGimp - Far West Minutemen - No AWKCR_No CROSS Cybernetics.  
Added You and What Army - But it's Other Factions.  
Added Ad Victoriam.  
Added Read Notes from Containers and Corpses.  
Added Crimsonrider's Accessories.  
Added West Tek Tactical Optics.  
Updated Sim Settlements 2.  
Updated SS2 Extended.  
Updated Workshop Framework.  
Updated Boston Natural Surroundings.  
Updated Pine Trees Redone.  
Updated M8r Complex Sorter.  
Updated M8r Complex Sorter output plugin.  
Updated Bodyslide Output.  
Updated Sim Settlements 2.  
Updated Workshop Framework.  
Updated Publick Occurrences Expanded.  
Updated F4 CK Fixes.  
Updated High FPS Physics Fix.  
Updated Buffout 4.  
Updated Wetness Shader Fix.  
Removed Agemo's NPCs.  
Removed Intimidation Perk Extended.  
Removed NXGEN - Nice Bush.  
Removed Better The Third Rail.  
Removed Fallout 76 Weather.  
Removed Private Military Company and all related patches.  
Removed Infinite Settlement Budget.  
Removed Quest Tweaks - Nuka World - Cappy in a Haystack.  
Removed Quest Tweaks - Nuka World - Precious Medals.  
Removed Supermutants Shall Inherit the Earth.  
Changed Reginald's Outfit to only be Underarmor.  
Changed Black Widow chest from Novice lock to Expert lock.  
ESL-flagged about 40 more plugins or so.  
Removed Magnum Opus - No PMC profile.  
Built so many goddamn precombines.  
Generated so much goddamn previs.  
Deleted so many goddamn trees.  
Various other small tweaks.

Gwen McNamara, Doctor Amari, and Tina DeLuca replacers now provided by keke-bu.  
Kasumi, Glory, and Scribe Haylen replacers now provided by Wasteland Heroines Replacer 2.  
Proctor Ingram replacer now provided by Wasteland Heroines Replacer 3.  
Professor Scara replacer now provided by Wasteland Heroines Replacer 4.  
Desdemona replacer now provided by Wasteland Heroines Replacer 5.

---

2021/04/04

Version 2.6.1

Added SS2 Traveling Visitors.  
Added F4 Creation Kit Fixes.  
Removed PAC - Project Apocalyptic Commonwealth.  
Updated fallout4custom.ini.

---

2021/04/02

Version 2.6.0

Updated Mod Organizer 2.  
Updated See Through Scopes.  
Updated SS2-XDI Patch.  
Updated Sim Settlements 2 - Tiny Living.  
Added Raider Gangs Extended.  
Added Sim Settlements 2 - Wasteland Reconstruction Kit.  
Added Wasteland Ventures Sim Settlements 2 Addon.  
Added SS2 Superstructures - A Sim Settlements 2 Addon.  
Added PAC - Project Apocalyptic Commonwealth.  
Removed Restore PA Frames.  
Slight changes to separators and organization in MO2's left pane.

---

2021/03/21

Version 2.5.4

Updated Sim Settlements 2.  
Updated Workshop Framework.  
Updated Rise of the Commonwealth - for SS2.  
Updated High FPS Physics Fix.  
Updated Bodyslide Output.  
Added Jamaica Plains Navmesh Fix.  
Changed Demolition Expert description to correctly point to the Explosives Workbench.  
Moved Refreshing Beverage from BEVERAGE - OTHER to AID category.  
Capitalized the R in "Reduced" for the M520 Long Trench Barrel omod description.  
Changed the name of the uzi from UZI to Uzi.  
Removed the double entry for Psychotats in the Chem station.  
Cleaned up the Utility entries that were still under the Chem station.  
Moved Vegetable Starch back to the Cooking station.  
Reduced counts on Fortune Finder lists.

---

2021/03/18

Version 2.5.3

Updated Whisper's Extra Pieces and Snaps.  
Updated M8r's Complex Item Sorter.  
Updated M8r Complex Sorter plugin for both profiles.  
Updated Buffout 4.  
Removed Spiff's Wasteland Clothing Pack.  
Removed Spiff's Wasteland Clothing Pack from CustomLLs.esp.  
Fixed more typos in David Hunter.  
Removed Hyde Park from being a possible radiant location in David Hunter's quest probably maybe i hope idk.  
Removed Achievements. Buffout handles this and I have successfully forgotten to remove this dll for like two months now. I FINALLY REMEMBERED THIS TIME.

---

2021/03/12

Version 2.5.2

Updated Sim Settlements 2.  
Updated Workshop Framework.  
Updated Better Companions - AIO.  
Updated Leaders and Legends of the New Commonwealth.  
Updated Intimidation Perk Extended.  
Added a few custom tweaks to Better Companions - AIO (changed affinity perks for Cait and Nick, respectively).  
Added Rise of the Commonwealth for SS2.  
Added Assault Marine Armor Redux.  
Created a custom patch for Assault Marine Armor Redux.  
Added 4estGimp - DefenseGun Fixes and R88 INNR Formatting  
Fixed previs issue in Hub City Auto Wreckers.  
Added Equip Slot 30 - Hair Top to Metal Skull Helmet.  
Added a new typo patch for Xander's Aid.  
Added a new typo patch for David Hunter - A Brotherhood Story.  
Recategorized Mysterious Serum in the Chemlab.  
Renamed Plasma Gun from "Plasma" to "Plasma Gun". Don't ask, I don't know.  
Removed Baka Interface and all related patches.

---

2021/03/02

Version 2.5.1

Updated High FPS Physics Fix.  
Updated Whisper's Extra Pieces and Snaps.  
Updated Complex Vendors.  
Reduced Flight Helmet defense rating from 30 to 3.  
Metal Helmet now requires Armorer Rank 1 to craft.  
Geneva's Outfit now requires Player to complete Getting a Clue to craft.  
Grognak Costume Replica now requires Player to complete quest stage 200 of The Silver Shroud to craft.  
Survivalist's Headgear Upgraded Filter now requires Science! Rank 1 to craft.  
Survivalist's Civilian Headgear Upgraded Filter now requires Science! Rank 1 to craft.  
Soviet Gas Mask now requires Science! Rank 1 to craft.  
Upgraded Gas Mask now requires Science! Rank 1 to craft.  
Soviet Survivalist's Civilian Headgear now requires Science! Rank 2 to craft.  
Rodeo Long Coat now requires Armorer Rank 2 to craft.  
Rodeo Long Coat Modest now requires Armorer Rank 2 to craft.  
Alice Long Coat now requires Armorer Rank 2 to craft.  
Apocalyptic Witch now requires Armorer Rank 3 to craft.  
Vault 81 Jumpsuit now requires the Player to have been inside Vault 81 to craft.  
Vault 81 Jumpsuit - New now requires the Player to have been inside Vault 81 to craft.  
Vault 81 Security Armor now requires the Player to have been inside Vault 81 to craft.  
Covenant Security Armor now requires the Player to have been to Covenant to craft.  
Covenant Security Helmet now requires the Player to have been to Covenant to craft.  
Helmeted Cage Armor now requires Player to complete An Ambitious Plan to craft.  
Helmeted Spike Armor now requires Player to complete An Ambitious Plan to craft.  
BoS Elder Coat Cut-off now requires Player to complete Call to Arms to craft.  
BoS Long Battlecoat now requires Player to complete Call to Arms to craft.  
BoS Long Battlecoat Vault Suit now requires Player to complete Call to Arms to craft.  
BoS Lancer Captain Coat now requires Player to complete Call to Arms to craft.  
All Wasteland Sniper gear now requires Armorer Rank 4 to craft.  
Scarves no longer require Armorer Rank 2 to craft.  
Greaser Jacket and Jeans now requires Atom Cats Garage to be completed to craft.  
Atom Cats Jacket and Jeans now requires Atom Cats Garage to be completed to craft.  
Atom Cats Vault Suit now requires Atom Cats Garage to be completed to craft.  
Bomber Jacket now requires Player to have visited the Prydwen to craft.  
Utility Jumpsuit [Brotherhood] now requires Player to have visited Prydwen to craft.  
Renamed Holotapes from Workshop Framework, Workshop Plus, Homemaker, and NPCs Travel.  
Fixed equip slots on Blue Batting Helmet.  
Sleepless Nights holotape moved to Settings.  
Restore Power Armor Frames holotape moved to Settings.  
Dirty Postman Uniform moved to OUTFITS - RUGGED crafting section in the Clothing workbench.  
Utility Jumpsuit [Railroad] can now only be found under OUTFITS - COVERALLS category in the Clothing workbench.  
Utility Jumpsuit [Railroad] now requires the Player to have completed Road to Freedom to craft.  
Utility Jumpsuit [Camo - Woods] moved to OUTFITS - COVERALLS in the Clothing workbench.  
Utility Jumpsuit [Camo - Urban] moved to OUTFITS - COVERALLS in the Clothing workbench.  
Utility Jumpsuit [Camo - Jungle] moved to OUTFITS - COVERALLS in the Clothing workbench.  
All Gunner Outfits now requires Player to clear GNN location to craft.  
Xander's Aid ammunition now requires Player to advance in the Xander's Aid quests to craft.  
Cannonballs now requires Player to complete Last Voyage of the U.S.S. Constitution to craft.  
All Venom Gun ammunition now requires Player to complete Hunter/Hunted to craft.  
Edited 5mm Rifle Round conversion recipe to be an even exchange of 50 5mm Rounds for 50 5mm Rifle Rounds.  
Edited 5mm Rifle Round conversion recipe to be properly sorted into the BULK ROUNDS - BALLISTIC (x50) category in the Ammunition workbench.  
Added 5mm Rifle Round recipe for the BULK ROUNDS - BALLISTIC (x10) category in the Ammunition workbench.


---

2021/02/23

Version 2.5.0

Added FO4 Photo Mode.  
Added Simple Clothing Keywords.  
Added Pain Train and Impact Landing - Buffed and Reworked.  
Added Hunkered Down.  
Added Lootable Vertibirds.  
Added Useful Technical Documents - Legendaries.  
Added Heavy Gunner Buffs Minigun Separately.  
Added Barefoot Footstep Extended.  
Added Better Notes.  
Added Publick Occurrences Expanded.  
Added Companion Active Wait.  
Added Leaf Piles Improved.  
Updated Sim Settlements 2.  
Updated SS2 Extended.  
Updated Workshop Framework.  
Updated Miniguns Rebirth.  
Updated High FPS Physics Fix.  
Updated Buffout 4.  
Updated Gunner Outfit Pack.  
Updated FallUI.  
Updated FallUI - Map.  
Updated Gunner Outfit Pack - Leveled List Integration.  
Updated Pine Trees Redone.  
Updated Jump Grunt.  
Updated Lively's Tweaks.

---

2021/02/05

Version 2.4.8

Removed 13a972 from Interior Lighting Enhanced AIO.

---

2021/02/04

Version 2.4.7

Updated Buffout 4.  
Updated High FPS Physics Fix.  
Removed Landscape Grass Fixes.

---

2021/02/03

Version 2.4.6

Updated FallUI Workbench.  
Updated Whisper's Extra Pieces and Snaps.  
Added Better Landscape Grass.  
Fixed visibility issue in RobCo Sales and Service Center.  
Fixed visibility issue in Monsignor Plaza.  
Updated MCM section in the ReadMe.  
Added small section of the ReadMe to address Pipboy Map settings for controller users.

---

2021/02/03

Version 2.4.5

Added Buffout 4.  
Removed Baka ScrapHeap.

---

2021/02/01

Version 2.4.4

Removed Buffout 4.  
Added Baka ScrapHeap.  
Updated Hollywood Laser Bolts.

---

2021/02/01

Version 2.4.3

Updated Buffout 4.  
Updated Miniguns Rebirth.  
Updated Whisper's Extra Pieces and Snaps.  
Updated Tales From the Commonwealth.

---

2021/01/31

Version 2.4.2

Added Sim Settlements 2 - Tiny Living.  
Added Jump Grunt.  
Added Commando Buffs Submachine Gun Separately.  
Added Miniguns Rebirth.  
Added Fixed Creature Death Drops.  
Added Sunlight Alignment Tweak - Better Dawn and Dusk.  
Updated Hollywood Laser Bolts.  
Updated Commonwealth Gunfire Overhaul.  
Updated High FPS Physics Fix.  
Removed Boston Natural Weathers. Maybe I'll try it again later but I don't really feel like swapping weathers at the moment.  
Removed equip slot 30 from Batting Helmet (f6d8c).  
Removed erroneously added perk requirements for Bloatfly Steak. Sorry about that.  
Changed Laser Musket's sound level from Loud to Very Loud.  
Slight adjustments to Lively's HUD Preset. Moved flashlight icon to rest atop the AP bar, moved dialogue box slightly upward, moved crit meter slightly downward.  
Changed pppl.ini. Same result, different equation. Doesn't matter.  
SO MANY LEVELED LIST ADJUSTMENTS.

---

2021/01/25

Version 2.4.1

Updated Sim Settlements 2.  
Updated Workshop Framework.  
Updated FallUI Workbench. Twice!  
Added (and then updated) Whisper's Extra Pieces and Snaps.  
Added Boston Natural Weathers. I'm not seeing much of a difference yet but we will see.  
Created Crafting-AtomGreatness.esp to address slight issues with keywords in the chemlab (this fixes the odd sorting menus for Holy Water and Holy Hand Grenade that nobody reported but I noticed it anyway, don't worry).  
Added custom object and accompanying crafting recipe for a Vault 81 Molerat Disease Cure.  
Removed an overly wordy loading screen from Wattz Laser Gun.  
Updated Immersive Power Armor HUD - T-45 and Raider.  
Updated CWSS Redux.  
Removed the Time To Say Goodbye note from LoreNotes.esp because I am sick of it spawning on multiple dead raiders and I'm too lazy to do a real fix for something I don't care that much about.  
Removed ss2 new stuff i found.esp.

---

2021/01/22

Version 2.4.0

Fixed conditions for Rugged Outfits. They should now appear in the workbench as expected. Probably. I didn't look in game.  
Fixed sorting and tagging for PlasRail weapons.  
Added Gunner Outfit Pack Standalone.  
Added Gunner Outfit Pack - NPC Leveled List Integration.  
Added Power Armor HUD Switcher.  
Added Power Armor HUD Switcher Update 1.1.  
Added Power Armor HUD Switcher Invisible 3rd Person.  
Added Immersive Power Armor HUD - T-45 WIP.  
Added Makconner's Spartan Cockpit - T-60 Cockpit 1.0011.  
Added Makconner's Spartan Cockpit - Spartan Cockpit 1.0006.  
Added Makconner's Spartan Cockpit - Raider Cockpit 1.00015.  
Added Immersive and Clever Power Armor HUD Dials and Gauges.  
Added PA Hud Blue.  
Added Power Armor Hud Visor.  
Added Power Armor Helmet Style Visor - Animated Hud with Invisible 3rd Person.  
Added Power Armor Helmet Style Visor - Dashless with Invisible 3rd Person.  
Updated M8r984f2's Complex Item Sorter.  
Updated FallUI.  
Regenerated M8r Complex Sorter.esp.  
Disabled Scrolling Doesn't Change POV. Doesn't seem to get along well with Custom Camera.

---

2021/01/18

Version 2.3.6

Forwarded various changes made in the main profile in the last update (2.3.5) into the No PMC profile.

---

2021/01/17

Version 2.3.5

Added a new keyword to separate 5.7mm ammo from 5mm ammo in the ammunition workbench.  
Fixed equip slots on Vault Riot armor for female Vault 81 guards.  
Adjusted load order for Interiors Enhanced.  
Updated NXGEN - Nice Bush.  
Updated LooksMenu.  
Added Settler Sandbox Expansion.  
Added Doors Not Walls.  
Removed Emogene Takes a Lover (redundant).  
Removed a static rifle from Immersive Beantown because if I see a rifle, I should be able to pick it up and shoot people with it, dammit.  
Removed one board from a window at Drumlin Diner because Trudy was talking to a board instead of Wolfgang and it was awkward.  
Rebuilt precombine and previs for DrumlinDiner worldspace cell because that's a thing you have to do when you remove a single wooden board.  
Fixed a landscape seam northwest of vault 111 via adding two large rocks because that's the kind of person I am.  
Made some edits to CustomLLs.esp (primarily in regards to potentially increasing modded weapon spawn rates). Enemies and cells will need to reset for this to take effect.  
Added Custom Camera. This is primarily because I like the FOV features it provides, but then I started playing with other settings and I kinda like it now.  
Added Barber and Surgeon Camera Fixes.  
Removed Immersive Burning Flamers and Molotovs.  
All versions of Sirius armor can no longer have extra armors or clothing equipped simultaneously (excluding helmets and gloves).  
Switched source download for TFTC because gdrive was giving me an unreasonably hard time.  
Updated readme's mcm settings for Custom Camera. I can probably automate this in the future. I don't feel like it right now.

---

2021/01/11

Version 2.3.4

Updated FallUI Workbench.  
Hid Codsworth's Companion Perk from Baka Interface Levelupmenu.  
Added Dark Sci Fi Vault Retexture.  
Added Pre-War Binoculars - Call In Fire Support Add-on.  
Hid Fire Support Add-on perk from Baka Interface Levelupmenu.  
Updated Sim Settlements 2.  
Added NXGEN - Nice Bush. And then updated it five times. No, I'm not kidding.  
Added The Ballistic Series - 2K.  
Updated M8r's Complex Sorting Script.  
Updated item sorting plugin.  
Fixed the Featured Item thing maybe? I think? Pretty sure.  
Removed Calamity Interiors.  
Added Interiors Enhanced - Darker Ambient Light and Fog.  
Added Fourville. THIS IS UNTESTED. I'm just testing it in my current playthrough so...whatever, I'm not deleting it just to compile with Wabbajack.  
B90 armor set no longer allows you to wear additional pieces of armor on top.  
Made some adjustments to fallout4prefs.ini and fallout4custom.ini for better performance probably.  
Fixed No PMC profile. Why do I keep this profile updated again? Does anyone use it?

---

2021/01/08

Version 2.3.3

Added FallUI Workbench.  
Added Better Sleep Wait Menu.

---

2021/01/08

Version 2.3.1

Updated masters on FallUI sorting esps for both profiles.

---

2021/01/08

Version 2.3.0

Updated Pipboy Display settings in Fallout4prefs.ini for a more hi res version.  
Set default hud color back to icy blue because I like it more than white.  
Updated SS2-XDI patch.  
Added Ruddy's Simple Sorter.  
Added R88 INNRs.  
Added MXPF.  
Updated FallUI.  
Added R88 Complex Sorting by m8r89 (FallUI author, edited RSS script).  
Removed Phoenix Keywords and all related patches.  
Removed Phoenix Simple Sorting Overhaul and all related patches.  
Removed all VIS tags and resources.  
Added Intimidation Perk Extended.  
Added Deirdre Bugfix.  
Added SS2 Magnusson Terminal Fix.  

---

2021/01/13

Version 2.2.1

Removed Scavenge Junk. I was only using one record from it anyway and it's kinda pointless to leave the modlist down for one leveled list.  
Disabled an erroneously active plugin in the main profile that should only be active in the No PMC profile.  
Updated readme for widescreen support issue with Baka Interface.

---

2020/12/31

Version 2.2.0

Added Pine Trees Redone - BNS. Thanks for the suggestion, Pelinal. Looks nice.  
Updated Sim Settlements 2.  
Updated SS2 Extended.  
Updated FallUI.  
Updated Baka Interface.  
Reactivated Baka Interface and its custom patches.  
Updated Hollywood Laser Bolts.  
Removed Pip Boy Dual Colors.  
Removed Workshop.swf file from Def_UI.  
Removed Bronze Mama Murphy Overhaul.  
Added Mama Murphy's preset from FOFW Redux.  
Removed .modgroups file from Unofficial Fallout 4 Patch.  
I've probably done other minor tweaks as well but I can't remember, I've been pretty depressed while working on this for the last few weeks.

---

2020/12/16

Version 2.1.2

Updated UFO4P.  
Disabled Baka Interface.  
Disabled both Baka patches.  
Adjusted ini files in No PMC profile to reflect the main profile.

---

2020/12/15

Version 2.1.1

Changed the default profile back to the... default profile.  
Re-activated Baka Interface + its patches.

---

2020/12/14

Version 2.1.0

Updated Unofficial Fallout 4 Patch.  
Updated Unofficial Fallout 4 Patch again.  
Updated Sim Settlements 2.  
Updated Workshop Framework.  
Updated FallUI.  
Updated FallUI again.  
Updated Hollywood Laser Bolts.  
Updated Hollywood Laser Bolts again.  
Set Archive Parsing to false by default.  
Temporarily disabled Baka Interface until some background issues are resolved. No ETA, plz don't ask.  
Note that Baka Interface may still be in your load order and simply unchecked. You can leave them alone. I'm still messing with it so I don't want to delete it. Wabbajack will probably see that and download it for you, too. Don't worry about it.

---

2020/12/09

Version 2.0.2

Fixed workshop mode crafting menu crash.

---

2020/12/08

Version 2.0.1

Removed outdated Pipboy Flashlight Patch.  
Fixed No PMC profile.

---

2020/12/08

Version 2.0.0

Removed Sim Settlements AIO.  
Removed Sim Settlements Mega Pack - Year One.  
Removed Salvage Beacons.  
Removed Useful Crank v2.0.  
Removed BS Defence.  
Removed Harvest Restrictions.  
Removed all presets.  
Removed esl flag from 512 Standalone Hair Colors.  
Removed Cleaned ESMs.  
Removed VIS-Perks.  
Removed Calamity Weathers.  
Removed Calamity Weathers - Vibrant Tweaks and More Weathers.  
Removed Calamity Weathers - Reverb Patch.  
Removed Small Map Markers.  
Removed Diamond City Ranch.  
Removed Pip Boy 2000 Mk VI.  
Added Sim Settlements 2.  
Added SS2 Extended.  
Added SS2 Workshop HUD Override.  
Added SS2-XDI Patch.  
Added Fallout 76 Weather.  
Added Perfect Landscape - High BA2 by Pfuscher.  
Added FallUI.  
Added Baka Interface.  
Added HUD Plus Plus.  
Added Active Effects on HUD.  
Added FastPipBoy (R2K's Gameplay Mods).  
Added Weapon Quickswap (R2K's Gameplay Mods).  
Added High FPS Physics Fix.  
Added Weapon Debris Crash Fix.  
Added Fortune Finder 4 Fix - Enhanced Bottlecap Mine.  
Added Useful Crank v1.5.  
Added Wait Anywhere.  
Added No More Gaps Under Junk Fences.  
Added Snappable Junk Fences.  
Added Leaders and Legends of the New Commonwealth.  
Added Dual Color Pipboy.  
Added zpatch.  
Added zpatch override.  
Updated Workshop Framework.  
Updated Lively's Tweaks.  
Reworked PhoenixKeywordsPatch for both profiles.  
Reverted back to Nanosuit Pipboy. I know some of you didn't like it...but I do, so there.  
New options selected for Pipboy Flashlight.  
Deleted cobjs for lacy underwear.  
Fixed some triple perk conditions on M520 cobjs (if you are not aware, Fallout 4 can only display 2 perk requirements while crafting, but you can add as many requirements as you want, so having more than 2 is incredibly confusing and misleading).  
Reduced global molotov drop rates.  
Fixed some bullshit volumetric lighting.

---

2020/10/13

Version 1.1.7

Changed molotov recipe to require Vodka instead of Glass and Oil.  
Reduced molotov hazard duration from 19 to 8.  
CROSS Cybernetics armors cannot be crafted until completing the Automatron DLC probably.  
Slight edits to the custom DEF UI preset.  
Removed Diamond City Auto Close Gate.  
Removed Vault 81 Close Door.  
Added No More Perk Popups - Silent Perks.  
Fixed Vault 81 Riot Guard Armor/Vault 81 Jumpsuit on female guards.  
Added sorting tags to Lacy Underwear.  
Updated Buffout 4.

---

2020/10/12

Version 1.1.6

Fixed NCR Ranger Mask CTD at the Armor Workbench.  
Updated Buffout 4.  
Updated Better Companions AIO.  
Rebuilt Lexington.  
Rebuilt Nahant.  

Please don't ask me about those last two things, I don't want to talk about it.

---

2020/10/03

Version 1.1.5

Added Smaller Map Markers.  
Added CCCleaner.  
Added Simply Lowered Drawbridges.  
Added Emogene Takes a Lover - Quest Fix.  
 - *Yes, I stole two of those from F4EE. I have no shame.*  
Fixed one house from BTI in Concord that 99% of you won't see because nobody even goes to that part of town anyway.  
Removed Super Mutant Explosion Resistance. (They still have high damage resist overall so keep that in mind before you say "But Lively, my 1000 damage mini nuke only does 600 damage, what gives")  
Updated Buffout 4.  
Slight change to xSE PluginPreloader.xml. This means you should copy Game Folder Files yet again.

---

2020/10/01

Version 1.1.4

DELETE xSE PluginPreloader.ini FROM YOUR FALLOUT 4 FOLDER.

If you have your workbase archives saved as a mod in MO2, make a backup of those first before updating.

Updated Buffout 4.  
Updated xSE PluginPreloader.  
Updated Game Folder Files. You need to copy these again if you're updating. Don't forget to delete the ini file mentioned above.  
Integrated the Uzi fix from the post above.  
M520 - Reduced Reload Speed by 20%, decreased damage by 33%.  
M520 Camo - Decreased Reload Speed by 20%, decreased damage by 39%.  
M520 Desert - Decreased Range by 33%, decreased damage by 60%.  
M520 Reaper - Decreased Reload Speed by 40%, decreased damage by 52%.  
Doubled material cost for everything in the clutter workbench.  
Brought the No PMC profile up to date with the main version.  
Removed accessories and underwear from settler leveled lists. This should solve the problem with naked settlers occasionally spawning.

---

2020/09/30

Version 1.1.3

Changed source download for ECD Fix.  
Deleted around 50 trees from Lexington, along with an entire building, a ghoul spawn, some random items, a gingerbread house, and some other things to make the city less stupid.  
Deleted those weirdo presets nobody cared about anyway.  
Deleted five trees from Nahant.  
Deleted some stupid invisible bridge thing in Malden Center.  
Deleted all the stupid damage modifier omods from various weapons (probably).  
Forgot to look at the uzi but I'm pretty sure I know what's going on so I'll fix it tomorrow but for now it's almost 2 am so plz be patient.

--

2020/09/28

Version 1.1.2

Removed Extreme Particle Overhaul.  
Updated Buffout 4.  
Updated Game Folder Files.  
Updated Classic Holstered Weapons System.  
Added custom MO2 splash screen (special thanks to @Thurisaz, they deserve all the praise for this neat little personal touch).

Don't forget to copy Game Folder Files again if you're updating. It is required.

---

2020/09/27

Version 1.1.1

Updated Overboss Helmet Lamp Fix.  
Updated Buffout 4.  
Adjusted Buffout 4 toml file to allow LooksMenu to work properly. I...do not yet know what other issues may arise from this.  
Removed Tank Tops from Wasteland Clothing Pack.  
Reduced Supermutant Health Regen from 3%/sec to 1%/sec.  
Reduced Supermutant Behemoth Health Regen from 4%/sec to 1.2%/sec.  
Reduced Supermutant & Behemoth Explosion Resistance by 50%.  
Readded Settlement Menu Manager because I am not particularly intelligent. You know it. I know it.  
Fixed previs issue in Concord with Subway Runner because there was a RECTANGULAR PLANE MARKER AROUND A CYLINDER-SHAPED WINDOW AND IT BROKE EVERYTHING IF YOU STEPPED INSIDE THE TINY LITTLE PLANE MARKER LIKE SERIOUSLY HOW DID YOU GUYS EVEN FIND THIS.  
Changed the default setting for blood spatter on screen to disabled.  
Changed default launcher settings to be borderless windowed.  

---

2020/09/25

Version 1.1.0

Added Redder Rocket.  
Added Master Plan.  
Added Stairs Ladders Ramps.  
Added The Cabin in the Woods.  
Added Box Houses  
Added Bob's Iguana Diner.  
Added Atom's Greatness.  
Added Pip-Boy 2000 Mk VI.  
Updated Buffout 4.  
Changed source for More Feral Ghouls.  
Implemented updated patches that were linked above.  

Still investigating video driver crashes. I don't have a solid solution yet. My sincerest apologies. I want this fixed just as much as you do.

---

2020/09/22

Initial release of Magnum Opus 1.0.0.

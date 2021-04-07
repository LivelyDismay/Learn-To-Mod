# Learning to Mod

- [Introduction](#introduction)
- [Modding Tools](#modding-tools)
  - [xEdit](#xedit)
  - [Creation Kit](#creation-kit)
  - [Mod Organizer 2](#mod-organizer-2)
      - [Disable the Steam Overlay](#disable-the-steam-overlay)
    - [Change Steams Update Behavior](#change-steams-update-behavior)
    - [Set the Game language to English](#set-the-game-language-to-english)
    - [Clean Skyrim](#clean-skyrim)
    - [Start Skyrim](#start-skyrim)
  - [Using Wabbajack](#using-wabbajack)
    - [Preparations](#preparations)
      - [Problems with Wabbajack](#problems-with-wabbajack)
  - [Post-Installation](#post-installation)
    - [Copy Game Folder Files](#copy-game-folder-files)
- [Updating](#updating)
- [Noteworthy Mods](#noteworthy-mods)
  - [Elder Souls - Death](#elder-souls---death)
  - [Camera](#camera)
  - [Combat - Melee](#combat---melee)
  - [Combat - Archery](#combat---archery)
  - [Combat - Magic](#combat---magic)
  - [Skills, Perks and More](#skills-perks-and-more)
  - [Quest and Encounter Mods](#quest-and-encounter-mods)
  - [Monster Mods](#monster-mods)
  - [Expanded Cities Towns and Villages](#expanded-cities-towns-and-villages)
  - [NPC Retextures](#npc-retextures)
  - [Followers](#followers)
  - [Audio and Weather](#audio-and-weather)
  - [New Equippables](#new-equippables)
  - [ENB: Ominous](#enb-ominous)
- [In-Game MCM Options](#in-game-mcm-options)
  - [Follower Framework](#follower-framework)
- [Creating your Character](#creating-your-character)
- [FAQ](#faq)
- [Tweaking Performance](#tweaking-performance)
  - [Tweaking the ENB](#tweaking-the-enb)
  - [Tweaking the Game Settings](#tweaking-the-game-settings)
- [Removing the Modlist](#removing-the-modlist)
- [Credits and Thanks](#credits-and-thanks)
- [Contact](#contact)
- [Contributing](#contributing)
- [Changelog](#changelog)

# Introduction

This will be a collection of various modding lessons, mostly revolving around how to read, use, and edit xEdit (SSEEdit and FO4Edit).

This project will be open source. I encourage anyone to contribute any knowledge they can to make this better for newcomers and veteran modders alike.

## Modding Tools

### xEdit

xEdit is a tool built for modding Bethesda Games, and is an all-encompassing term to refer to multiple programs, such as SSEEdit, TESEdit, and FO4Edit. They are all the same exact program. Renaming the .exe itself (or adding a custom argument when running the .exe) will allow it to be used on the game of your choice.

### Creation Kit

Official engine software released by Bethesda Game Studios. The Creation Kit is what is used to make the game in its entirety. Some time after release, Bethesda releases a stripped-down version of the CK for modders to use.

### Mod Organizer 2

Used for downloading, installing, organizing, and editing mods. Launches all installed files through a Virtual Directory in order to keep your game's installation folder as untouched as possible.

##### Disable the Steam Overlay

The Steam Overlay can cause issues with ENB and is recommended to be turned off.

Open the Properties window (right click the game in your Library->Properties), navigate to the _General_ tab and un-tick the _Enable the Steam Overlay while in-game_ checkbox.

#### Change Steams Update Behavior

SSE is still being updated by Bethesda (they only add Creation Club content). Whenever the game updates, the entire modding community goes silent for the next one or two weeks because some mods need to be updated to the latest game runtime version.

To ensure that Steam does not automatically updates the game for you, head over to the Properties window, navigate to the _Updates_ tab and change _Automatic updates_ to _Only update this game when I launch it_. You should also disable the Steam Cloud while you're at it.

#### Set the Game language to English

Just do it. This entire Modlist is in English and 99% of all mods you will find are also in English. I highly recommend playing the game in English and **I will not give support to people with a non-English game**.

Open the Steam Properties window, navigate to the _Language_ tab and select _English_ from the dropdown menu.

#### Clean Skyrim

I highly recommend uninstalling the game through Steam, deleting the game folder and reinstalling it. You should also clean up the `Skyrim Special Edition` folder in `Documents/My Games/`.

#### Start Skyrim

After you have done everything above and got a clean SSE installation ready, start the Launcher and open the _Options_ menu.

1. Click on _High_
2. Set the _Aspect Ratio_ and _Resolution_ to your monitor's native values
3. Set _Antialiasing_ to _Off_
4. Check _Windowed Mode_ and _Borderless_

Start the game and exit once you're in the main menu.

### Using Wabbajack

#### Preparations

Let's get to the actual installation..

Grab the latest release of Wabbajack from [here](https://github.com/wabbajack-tools/wabbajack/releases). You need to download the `Wabbajack.exe` file ONLY. Place the `Wabbajack.exe` file in a blank folder at the root of a drive, such as `C:/Wabbajack`.

Launch Wabbajack. When it is finished extracting and installing itself, select the `Browse Modlists` option. Click the Download arrow for Elder Souls, and you will be forwarded to the next screen when it is finished.

Set the `Installation Location` to a blank folder at the root of a drive, such as `D:\Elder Souls`. The `Download Location` will update automatically.

Click the `Play` arrow.

##### Problems with Wabbajack

There are a lot of different scenarios where Wabbajack will produce an error. I recommend re-running Wabbajack before posting anything. Wabbajack will continue where it left off so you loose no progress.

**Could not download x**:

If a mod updated and the old files got deleted, it is impossible to download them. In this case just wait till I update the Modlist.

**x is not a whitelisted download**:

This can happen when I update the modlist. Check if a new update is available and wait if there is none.

**Wabbajack could not find my game folder**:

Wabbajack will not work with a pirated version of the game. If you own the game on Steam, go back to the [Pre-Installation](#pre-installation) step.

### Post-Installation

#### Copy Game Folder Files

Download the latest ENB Series from [here](http://enbdev.com/download_mod_tesskyrimse.htm) and copy `d3d11.dll` and `d3dcompiler_46e.dll` to your game folder.

Copy the all of the files from the `MO2/Game Folder Files` directory into your game folder.

## Updating

If this Modlist receives an update please check the Changelog before doing anything. Always backup your saves or start a new game after updating.

**Wabbajack will delete all files that are not part of the Modlist when updating!**

This means that any additional mods you have installed on top of the Modlist will be deleted. Your downloads folder will not be touched!

Updating is like installing. You only have to make sure that you select the same path and tick the _overwrite existing Modlist_ button.

## Noteworthy Mods

### Elder Souls - Death

This mod implements the Soulsborne-style leveling and death system into Skyrim. Gold is used as a substitute for Souls. When you sleep in a bed, you will be able to spend your current gold to level up your skills. You may also use training books to increase your skills. To level up, you must sleep in a bed.

Additionally, upon sleeping in an owned or rented bed, that location will be marked as your current Respawn Point. On death, a Gravemarker will be spawned at your location containing all of your currently held gold, and you will be teleported to your most recent Respawn Point. If you die again, your previous Gravemarker will be replaced, and the original Gravemarker will be unobtainable.

Your ability to save is limited as well. To save the game, you must sleep in a bed. When you activate a bed, you will be given an item called Elder Scroll - Break. This is a one-time consumable that will allow you to save once wherever you wish.

### Camera

This little section will go over some of the installed mods that effect the camera in a subtle or substantial way. They get their own section because it can feel very weird playing with them for the first time.

[SmoothCam](https://github.com/mwilsnd/SkyrimSE-SmoothCam) overhauls third person camera movement to make it feel more like a typical action adventure type camera. It's fully configurable via MCM; tweak it till things feel right.

### Combat - Melee

[Blade and Blunt](https://www.nexusmods.com/skyrimspecialedition/mods/34549) is a streamlined combat overhaul designed to enhance Skyrim’s difficulty and encourage active resource management. Unlike other combat overhauls, it does not seek to import mechanics from other games into Skyrim. Instead, it enhances the existing mechanics of Skyrim’s combat and focuses on tightening the gameplay to allow for more player skill and RPG-like character development.

You should read this mod page.

### Combat - Archery

[Legendary Skyrim Crossbows](https://www.nexusmods.com/skyrimspecialedition/mods/8273) adds in crossbows as a full crossbow weapon expansion to Skyrim. There are crossbows for each material type, artifact crossbows, faction crossbows and they have been added seamlessly into the whole of Skyrim. Enemies now have a chance of using crossbows and you will find them just like you would any other type of weapon.

### Combat - Magic

[Mysticism](https://www.nexusmods.com/skyrimspecialedition/mods/27839) completely overhauls and rebalances vanilla magic while adding in 200ish new spells to flesh things out a bit.

[Forgotten Magic Redone](https://www.nexusmods.com/skyrimspecialedition/mods/12711) provides a unique and build defining progression system for magic users. Additionally there are many new spells added by the various content mods ranging from summons to elemental based magic.

### Skills, Perks and More

[Wintersun](https://www.nexusmods.com/skyrimspecialedition/mods/22506) adds religion and worship.

I chose [Adamant](https://www.nexusmods.com/skyrimspecialedition/mods/30191) for our perk overhaul since it pairs so very nicely with both Mysticism and Blade and Blunt by the same author.

Werewolves are overhauled by [Growl](https://www.nexusmods.com/skyrimspecialedition/mods/31245) while [Curse of the Vampire](https://www.nexusmods.com/skyrimspecialedition/mods/10086) takes care of our bloody friends of the night.

[Aetherious](https://www.nexusmods.com/skyrimspecialedition/mods/26686) is a streamlined race overhaul designed to make races more meaningful without making them more restrictive.

[Shout](https://www.nexusmods.com/skyrimspecialedition/mods/12149) improves upon all shouts in Skyrim in a fair and balanced way by cutting down the cooldown timer effects, thus allowing the player to use a host of shouts in innovative, devastating combinations.

[Mundus](https://www.nexusmods.com/skyrimspecialedition/mods/33411) is a streamlined Standing Stone overhaul designed to ensure that every stone fills a niche and offers competitive bonuses to different playstyles.

### Quest and Encounter Mods

Elder Souls comes with a wide variety of new quest and encounters.

[Beyond Reach](https://www.nexusmods.com/skyrimspecialedition/mods/3008) is a DLC sized mod that takes place in the east of High Rock, commonly known as The Reach. Beyond Reach is a dark story of intrigue and conspiracies sown by both men and gods as well as the struggles of those in the most squalid of situations.

[Darkend](https://www.nexusmods.com/skyrimspecialedition/mods/10423) allows you to travel to the new island of Pharos, explore detailed environments, fight new enemies and discover an Ancient set of weapons of incredible power. There is no quest or hand holding and is heavily inspired by the Soulsborne games.

[Vigilant](https://www.nexusmods.com/skyrimspecialedition/mods/11849), [Glenmoril](https://www.nexusmods.com/skyrimspecialedition/mods/32998) and [Unslaad](https://www.nexusmods.com/skyrimspecialedition/mods/11789) are an interconnected set of super mods that add a dark and awesome storyline with a ton of Soulsborne inspired content. Glenmoril is still in development but it's worth adding for the current content. Vigilant and Glenmoril creatures and items have been integrated into the rest of the game.

[Forgotten Dungeons](https://www.nexusmods.com/skyrimspecialedition/mods/449) adds over sixty new radiant quest enabled dungeons with entirely new monsters to encounter. It has been updated to pull in additional monsters from the Elder Souls monster merge.

[Hammet's Dungeons](https://www.nexusmods.com/skyrimspecialedition/mods/12186) and [Land of Vominheim](https://www.nexusmods.com/skyrimspecialedition/mods/31472) add another 60ish high quality dungeons and a landmass the size of solstheim to explore.

[Missives](https://www.nexusmods.com/skyrimspecialedition/mods/17576?tab=files) adds a large number of localized radiant quests found at Missive Boards of varying difficulty and with varying rewards. Missives has been extended to Solstheim.

[Skyrim Sewers](https://www.nexusmods.com/skyrimspecialedition/mods/9320) adds an accessible sewer system to the towns of Solitude, Whiterun, Windhelm and Markarth and also small sewage tunnels to Fort Sungard and Greenwall. Don't let the name fool you as this is by far some of the best made dungeon content available for Skyrim.

[Bleak Falls Barrow - Revisited](https://www.nexusmods.com/skyrimspecialedition/mods/33251), [Embershard Mine - Revisited](https://www.nexusmods.com/skyrimspecialedition/mods/34468), [Steepfall Burrow - Revisited](https://www.nexusmods.com/skyrimspecialedition/mods/34594) and [Ustengrav - Revisited](https://www.nexusmods.com/skyrimspecialedition/mods/33878) adds some new spice to the tired old dungeons that we've all done a hundred times. Enjoy!

### Monster Mods

I've included a variety of hand placed monster encounters from various people including mihail and opusglass. I mostly focused on dark fantasy, horror, soulsborne type content when possible. There are too many mods to list them all out here so just check the modlist itself. Monsters from this massive monster merge have been distributed all throughout the game including some of the mod added content like Forgotten Dungeons.

[Sea of Spirits](https://www.nexusmods.com/skyrimspecialedition/mods/4781) turns the Sea of Ghosts (and the rest of the seas in Skyrim and Solstheim) into a lively Sea of Spirits by adding many new sea creatures, like whales, narwhals, sharks, dreugh, and many others. Snow whale has been removed.

Draugr's have been given an overhaul via [Briraka's Draugr Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/26188), [Cannibal Draugr on Solstheim](https://www.nexusmods.com/skyrimspecialedition/mods/21238) and [Draugr Upgrades and Improvements](https://www.nexusmods.com/skyrimspecialedition/mods/21775)

### Expanded Cities Towns and Villages

Elder Souls comes with a massive merge of housing cities towns and villages that overhaul all of the population centers. The list is literally too long to go into in the readme so feel free to check the mod list. There are atleast four new player houses per hold ranging from small shacks to massive build your own settlements. The keys for these houses are all purchaseable, found at the end of quests or on enemy corpses. In addition to all of the housing every village town and city has been completely overhauled via a variety of mods.

### NPC Retextures

I love the work of [Pandorable](https://www.nexusmods.com/skyrimspecialedition/users/41216925) and used [Pandorable's NPCs](https://www.nexusmods.com/skyrimspecialedition/mods/19012), [Pandorable's NPCs - Dragonborn](https://www.nexusmods.com/skyrimspecialedition/mods/30680), [Pandorable's NPCs - Dawnguard](https://www.nexusmods.com/skyrimspecialedition/mods/24135) as my goto NPC retextures.

The Bijin lineup with [Bijin Wives](https://www.nexusmods.com/skyrimspecialedition/mods/11247), [Bijin NPCs](https://www.nexusmods.com/skyrimspecialedition/mods/11287) and [Bijin Warmaidens](https://www.nexusmods.com/skyrimspecialedition/mods/1825) fills the gaps that Pandorable's mods leave.

[The Men of Winter](https://www.nexusmods.com/skyrimspecialedition/mods/10902) retextures some Men in Skyrim. I handpicked NPCs from [The Ordinary Women](https://www.nexusmods.com/skyrimspecialedition/mods/12376) and [Kalilies NPCs](https://www.nexusmods.com/skyrimspecialedition/mods/30247). The rest is covered by [Diversity](https://www.nexusmods.com/skyrimspecialedition/mods/5291) and [Fresh Faces](https://www.nexusmods.com/skyrimspecialedition/mods/13789). [Ethereal Elven Overhaul](https://www.nexusmods.com/skyrim/mods/24273) is the base for all elves.

The priority looks like this (similar to MO2, the ones at the bottom overwrites the ones at the top):

1. Ethereal Elven Overhaul
2. Fresh Faces
3. Diversity
4. Kalilies NPCs
5. The Ordinary Women
6. The Men of Winter
7. Bijin NPCs
8. Bijin Warmaidens
9. Bijin Wives
10. Pandorable's NPCs
11. Pandorable's NPCs - Dragonborn
12. Pandorable's NPCs - Dawnguard
13. Simple Children

[Modest Elderly](https://www.nexusmods.com/skyrimspecialedition/mods/7935) protects the modesty of our elders.

### Followers

[Daanik the Returned](https://www.nexusmods.com/skyrimspecialedition/mods/21728/) is a powerful lich boss that you can summon to fight for you assuming that you can defeat him in combat.

[Inigo](https://www.nexusmods.com/skyrimspecialedition/mods/1461) is a fully voiced khajiit adventuring companion with over 7000 lines of unique dialogue - much of it about you. He'll level alongside you and avoid most traps. If you're sneaking he won't chatter and he'll whisper if you talk to him. He can run out of arrows. He's highly skilled in archery, one-handed, and sneak.

[Lucien](https://www.nexusmods.com/skyrimspecialedition/mods/20035) is a fully voiced Imperial follower with around 3000 lines of immersive, lore-friendly dialogue. Though he arrives in Skyrim as a cowardly scholar, he'll gradually gain strength and confidence by your side until he grows into a hero in his own right.

[Song of the Green - Auri Follower](https://www.nexusmods.com/skyrimspecialedition/mods/11278) is a fully voiced follower and quest mod, which centers around Bosmer culture and tradition. Auri, a traditionalist Wood Elf archer, will follow you, do your bidding, and offer occasional snarky commentary about your surroundings and actions.

[The Pale Lord](https://www.nexusmods.com/skyrimspecialedition/mods/21003) is a uniquely designed vampire follower with both a custom appearance featuring claws and a black textured outfit as well as scripted powers which include the ability to transform into a swarm of bats as well as being able to assume a monstrous War-form.

In addition to the above custom followers all of the vanilla followers have been overhauled by [Special Edition Followers](https://www.nexusmods.com/skyrimspecialedition/mods/7622) to fill unique roles as combat companions.

### Audio and Weather

[Audio Overhaul Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/12466) and [Immersive Sounds Compendium](https://www.nexusmods.com/skyrimspecialedition/mods/523) offer an amazing base for skyrim's ambiance and foley.

[Soulmancer Music Merge](https://www.nexusmods.com/skyrimspecialedition/mods/22551) thoughtfully merges soundtracks of Celtic Music, Extra Music, Musical Lore, Hun Lovaas, Still, Melodies of Civilization, Vindsvept, Northern & Southern Diaries, Fanmade Nordic Music, Dreams and Nightmares, Elder Songs, Dawn of Hope, and JDR. Additional tracks from Enderal, Two Step's From Hell, Icewind Dale and Baldur's Gate series!

[Dark Souls 3 Main Menu Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/23180) and [Dark Souls Sound Overhaul](https://www.loverslab.com/files/file/990-dark-souls-sound-overhaul/) replace the main menu background, main menu music and various UI sounds with those from Dark Souls.

The full Enigma series minus Disciple of Molag Bal from [Satafinix](https://www.nexusmods.com/skyrimspecialedition/users/21706239?tab=user+files) is used to overhaul dragonic and daedric voices. While other odds and ends update draugr voices, skeleton sounds and the like.

[Obsidian Weathers and Seasons](https://www.nexusmods.com/skyrimspecialedition/mods/12125) provides sharp, ominous, and atmospheric weathers that accentuate proximal detail while obscuring distant landscapes with mysterious fogs.

### New Equippables

All of the Dark Souls weapons from [FunkyGandalfCat](https://www.nexusmods.com/skyrimspecialedition/users/31528195) have been added as well as those from the [Dark Souls 3 Weapon Pack](https://www.loverslab.com/files/file/6203-dark-souls-3-weapon-pack/) Currently the DS3 weapon pack is craft only but will eventually become loot hand placed in the various new dungeons.

In addition to the above Glenmoril, Darkend, Unslaad and Vigilant add in many more Soulsborne flavored weapons, armor and jewelry.

[Heavy Armory](https://www.nexusmods.com/skyrimspecialedition/mods/15394) adds nearly 100 new weapons to Skyrim. You will find all new Halberds, Spears, Glaives, Shortswords, Quarter staves, Mauls, Hatchets and Clubs. These weapons are fully integrated into the rest of the game.

[Animated Armoury](https://www.nexusmods.com/skyrimspecialedition/mods/15394) adds halberds, rapiers, claws, pikes, quarterstaves and chain whips along with entirely new third and first person animations for each. These new animations have been extended to the relevant weapons from Heavy Armory and other content. All of these weapons have been fully integrated into the game.

[Skyrim Weapon Expansion](https://www.nexusmods.com/skyrimspecialedition/mods/32500) integrates over 100 high quality and balanced weapon variants into the vanilla game through crafting and leveled lists.

[Cloaks of Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/6369), [Divine Cloaks](https://www.nexusmods.com/skyrimspecialedition/mods/9304), [Daedric Cloaks](https://www.nexusmods.com/skyrimspecialedition/mods/9530) and [Artesian Cloaks of Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/17416) provide pretty physics enabled capes and integrates them into the world.

[Legendary Skyrim Crossbows](https://www.nexusmods.com/skyrimspecialedition/mods/8273) is a full crossbow expansion for Skyrim. There are crossbows for each material type, artifact crossbows, faction crossbows and they have been added seamlessly into the whole of Skyrim. Enemies will now have a chance of using crossbows and you will find them just like you would any other type of weapon.

[Warmonger Armory](https://www.nexusmods.com/skyrimspecialedition/mods/17809) aims to add immersion to your Skyrim experience adding new lore friendly Armors, Weapons and Clothes for both Vanilla Game and DLCs. All the added content is inspired from the classic Elder Scrolls Archetypes and is made with compatibility in mind.

[Common Clothes and Armors](https://www.nexusmods.com/skyrimspecialedition/mods/21305) is a combined and continued version of Common Clothes and Brigandage. It features 51 new armors and 80 new clothes, created by Franklin Zunge. The clothes are worn by the common people of Skyrim: Farmers, merchants, miners, patrons, workers and some of the wealthier citizens. They can also be bought at Radiant Raiment. The armors are worn by bandits. Since all new armors cover the whole body, half-naked bandits chilling in the cold climate of Skyrim are almost completely eliminated. The armors can be improved at a workbench, but they cannot be crafted or bought.

### ENB: Ominous

[Ominous](https://www.nexusmods.com/skyrimspecialedition/mods/27333) brings a grim feel to the world of Skyrim with its gloomy color palette, subtle lighting and dark skies.

## In-Game MCM Options

Everything not listed below is already configured for you. Feel free to peruse the settings and change them as you like.

### Follower Framework

- System
  - Load from File
  - Hotkeyed Abilities
    - Customize as you wish

## Creating your Character

Simply step up to the statue of mara and choose a start.

## FAQ

- My character is stuck dodging

  - This happens occasionally on load but rarely in gameplay. Press 'G' to fix it.

- I'm a 21:9 resolution user and my screen looks weird
  - Search 21x9 in mod organizer and activate all of those mods. Do this before creating your character or you'll need to do alot of configuration to get the UI looking right!!

## Tweaking Performance

My Setup:

- Ryzen 1700 running at 3GHz
- 1080ti
- 32GB DDR4-3200 RAM (CL 14)
- Game and MO2 running on a Samsung 850 EVO SSD

### Tweaking the ENB

This should always be the first thing you tweak. Disabling the ENB entirely can give you anything from 20 to >70 FPS. The ENB this Modlist comes with (see [ENB: Ominous](#enb-ominous)) is rather performance intensive. Open the ENB GUI using `Right Shift + Enter` (`Right Shift` is under the `Enter` key). This will open up the ENB GUI where you can enable and disable certain effects in the left panel.

- `Bloom`: Can give you up to 3 FPS, will make light sources less bright
- `DepthOfField`: Can give you up to 10 FPS, disabled by default and not really suited for gameplay
- `Ambient Occlusion`: This one is a big hitter. You can get up to 20 FPS by disabling this but the effect is very noticeable
- `Distant/DetailedShadow`: Those two can really give you a lot of FPS back depending on your shader settings (game settings). They are very noticeable.
- `ComplexFire/ParticleLights`: You won't see a lot of difference at first when disabling those two, but when particles are on screen (eg using magic or near light sources such as fires), they can _burn_ through your FPS

### Tweaking the Game Settings

I highly recommend using [BethINI](https://www.nexusmods.com/skyrimspecialedition/mods/4875) which is included in this Modlist (can be found in `MO2/tools/BethINI`). I recommend tweaking the `Detail` section for more FPS:

- `Shadow Resolution`: Very big one. A good balance is `2048` which is the borderline between high FPS drainage and garbage looking shadows.
- `Ambient Occlusion`: Highly recommended to leave this at `None`. The ENB this Modlist comes with, uses the ENB SAO which is 10x better and performance friendly than base game SAO.
- `Detailed Draw Distance`: Maybe try `2000` instead of `2800` but you won't notice a lot of FPS gain (maybe 1-3)
- `Remove Shadows`: If you really struggle, use this. This will disable all Shadows (not recommended)

## Removing the Modlist

You can just remove the MO2 folder and be done with it. SKSE and ENB files will still be in your game folder so I recommend using [ENB and ReShade Manager](https://www.nexusmods.com/skyrimspecialedition/mods/4143) if you want to remove the ENB.

## Credits and Thanks

- _YOU_ for actually reading the readme. Thanks a ton!!
- The Phoenix Flavor by Phoenix - General ideas and awesomesauce derived therefrom
- Lotus by erri120 - Repository template and NPC visuals
- Total - Being a really helpful guy.
- Halgari and everyone the WJ Team - Wabbajack is awesome and so are you
- KentuckyFriedCrusade - Thanks for the great work on the main menu and dark mode ui!!

## Contact

While I'm always available on the [Wabbajack Discord](https://discord.gg/wabbajack), I would advise checking the [Issues](https://github.com/jdsmith2816/eldersouls/issues) (open **and** closed ones) on GitHub first if you have any problems. The same goes for _Enhancements_ or _Feature/Mod Requests_. **DO NOT DM ME ON DISCORD. I WILL NOT PROVIDE SUPPORT FOR YOU IN DMS AND I WILL BLOCK YOU**.

## Contributing

See [Contributing](CONTRIBUTING.md).

## Changelog

See [Changelog](CHANGELOG.md).

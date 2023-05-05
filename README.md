2023-05-05 wow ui fresh install video + maintenance tips


----
***prepping a wow ui video in order to have a set process to set everything up on a new machine / new installation / for moving distros / other people to manage their whole ui instead of just pushing a WTF folder***


# ***-- 0. --***
to start off WoW install: 
go to: https://www.blizzard.com/en-us/apps/battle.net/desktop

within bnet install WoW Retail
this will result in creating a install folder structure like


# ***-- 1. -- UI manipulation through local files***
### - 1.1 FONTS
TODO: share the default font replacements - note: I use Expressway

### - 1.2 INTERFACE folder


texture replacement packs (BIG topic, lots of work here)
- https://www.tukui.org/addons.php?id=202 for login screen (i use Grey > Transparent)
- https://www.tukui.org/forum/viewtopic.php?f=11&t=30&start=50 use *No border with low background* for chat bubble
- icon replacement packs for 1px border squared icons everywhere https://github.com/AcidWeb/Clean-Icons-Mechagnome-Edition


### - 1.3 chat tabs / channels +++ Edit Mode scaling (maybe mention my UI Scale WA) note: start referring to JarUI
https://github.com/247jar/JarUI/blob/main/chat-cache.txt



***-- 2. -- managing addons***


### - 2.1 -- ***ElvUI wago.io collection***: https://wago.io/lw05cBLC4


----
# JarUI ElvUI approach:
- save performance *and* reduce dependencies by disabling many ElvUI modules.
- using ActionBars to mimic center WeakAura groups (because 1. ***snappiness of ElvUI actionbars*** and 2. rectangular icons and 3. bigger stack count text!) 
- designed to be pixel-perfect compatible with ``https://wago.io/NaowhUI-ClassWA`` (using Group Scale 1.1)
- ``https://wago.io/SJNeRkn47`` - ***must import ElvUI Private (Character Settings)*** for each character as well! (I have a lot of ElvUI modules disabled to get better performance, like default Blizzard UI skinning, map/minimap, chat, databars/texts, buffs/debuffs and more...)

## Short list of ElvUI modules that are being used (no other plugins!):
- General
- ActionBars
- Tooltip
- Unitframes

## To make this approach work, I instead use:
- Icon texture replacements: ``https://github.com/AcidWeb/Clean-Icons-Mechagnome-Edition``
- WoW login screen ***and*** ingame panel texture replacements: ``https://www.tukui.org/addons.php?id=202`` (Grey > Transparent)
- Chat bubble minimalist reskin: ``https://www.tukui.org/forum/viewtopic.php?f=11&t=30&start=50`` (use *No border with low background for chat bubble*)

## ***I recommend WowUp with CurseForge to keep all addons updated with just 1 click - yes, including ElvUI: ``https://wowup.io/``***

### A few addons that are quite practical and well maintained in Dragonflight:

- `AdiBags` (is my bag addon of choice because ***C A T E G O R I E S***)
- `AdvancedInterfaceOptions` (offers a nice ingame CVAR browser + lowlevel interface options)
- `Angry Keystones` (TODO: why do I use this one?)
- `Astral Keys` (TODO: why do I use this one?)
- `BetterCharacterPanel` (for character panel: to display Item Level *and* Enchant, Socket info per equipped item *and* on Inspect frame too!)
- ``BigWigs Bossmods`` (the boss timer addon with the fastest updates) + ``BigWigs_Voice`` + ``LittleWigs``
- `BlizzMove` (to actually be allowed to move ***all Blizzard panels***, *yes even the Exit Game menu*)
- `BtWQuests` (TODO: maybe if u wanna complete all the questlines)
- `BugGrabber` and `BugSack` (as LUA debug tools for all WoW addons)
- `Can I Mog It?` (to keep track of transmogs)
- `DejaCharacterStats` (for character panel: to see Equipped Item Level / Max Item Level for LFG)
- `Details! Damage Meter` (***TODO: SHARE PROFILE***)
- `Echo Raid Tools` (adds a icon for guild Echo's WeakAuras to import ingame in the adventure guide)
- `ElvUI` (***PROFILE: https://wago.io/lw05cBLC4***)
- `FPS-MS-Tracker` (to display a tiny, *class-colored* fps and ms counter on the bottom left-hand corner)
- `LS: Glass` (to have ***nice*** chat message animations and tab glow)
- ``Method Raid Tools`` (for raid CD tracking ***TODO: SHARE PROFILE***)
- ``Mythic Dungeon Tools`` (to edit, import & share M+ dungeon routes ***TODO: EXPLAIN M+ LIFE - keystone.guru, raider.io, getting MDT strings from streamers, big pushers.... all that fun***)
- `Narcissus` (to have a very modern, gorgeous character display)
- `OPie` (for a selection ring around your mouse cursor)
- `OmniCD - Party Cooldown Tracker` (for party cooldown + interrupts tracking -- ***TODO: SHARE PROFILE***)
- `Outfitter (Equipment Manager - Nulian's Fixed)` (the new Dragonflight version - to click on equipped item and immediately see replacement options inside character panel!)
- `Paragon Reputation` (for old Legion reputation paragon chests)
- `Pawn` (simplistic item upgrade hints in the tooltip)
- `Plater Nameplates` (THE addon for WoW nameplates. ***EXPLAIN: go to wago.io to import Plater profiles - mention Jundies, Naowh Twitch sub, etc.***)
- `Prat 3.0` (to modify chat text)
- `Premade Groups Filter` (to have more functionality in filtering through the LFG queue)
- `Project Azilroka` (***only use Enhanced Friends List***... disable all other modules!)
- `RCLootCouncil` (to ingame manage loot distribution... ***maybeeee explain Droptimizer, WoWaudit, blekfjbnsejikf bnsikjf nsuikdf b***)
- `Raider.IO` (to display https://raider.io/ scores, past keys in tooltip in LFG)
- `RareScanner` (to get alerts of rares and more map options like more map icons, dungeon/raid entrances)
- `SavedInstances` (to get an overview list of all relevant alts with their info, like lockout, weeklies, M+ keys etc.)
- `SharedMedia` (offers a framework to share addon resources, like textures, sounds, etc.)
- `SharedMedia_Causese` (most https://wago.io imports rely on this SharedMedia by Causese for alerts etc.)
- `Simulationcraft` (to type "/simc" ingame for a quick character data sheet to paste into https://www.raidbots.com/simbot/droptimizer )
- `Talent Loadout Ex` (to save many more talent tree Strings)
- `Talent Tree Tweaks | Dragonflight` (to make the talents panel smaller, transparent etc. - and more by Numedain)
- `Talent Tree Viewer (calculator) | Dragonflight` (to see other classes' talent trees, by Numedain)
- `TeleportCloak` (reliably & automatically re-equipps previous cloak after using any Teleport Cloak in the game)
- `TomTom` (THE addon for questing, offers an arrow, coordinates, /-commands)
- `WarpDeplete` (THE most complete Mythic+ dungeon timer)
- ``WeakAuras`` (THE framework to add UI work shared on https://wago.io )
- `World Quests List` (THE best world quest addon, displays listing of ALL available WQs next to the world map)



### - 2.2 -- ***share WowUp.io CF string***
https://github.com/247jar/JarUI/blob/main/WowUpio_CF_string.txt



### - 2.3 -- ***all the AddOn profiles*** TODO: complete list of addons and share their profiles on github

share each individual addon profile....





# ***-- 3. -- getting & sharing ui***
- https://wago.io/ biggest platform to share String / text based profiles for most popular addons (WeakAuras, Plater, ElvUI, Blizzard Edit Mode)
### - 3.1 -- make selection of recommended imports


https://wago.io/sTjueyP4U
https://wago.io/v5bS71bMj
https://wago.io/dmui-dragonriding
https://wago.io/jNjrKl3US
https://wago.io/p/Causese
https://wago.io/pogAL95VQ
https://wago.io/n7l5uN3YM
https://wago.io/NaowhUI-ClassWA # ***TODO: explain import process for Naowh dependency***
https://wago.io/z-SB3ciWq/ TODO: update for season 2?
https://wago.io/RaidAbilityTimeline
https://wago.io/TamasDragonflightHelper
https://wago.io/dfdungeons
https://wago.io/KrId6eJY6
https://wago.io/interruptorderNEW
https://wago.io/XEtM8dg1b
https://wago.io/ltENrybhU
https://wago.io/8Kge4dx6U TODO: find new CR BL tracker // + healer mana?
https://wago.io/Wa4_j1SIX



# ***-- 4. -- popular DISCORDS for WoW UI***
naowh, atrocity, tukui, etc...........
TODO collect all of them
explain subbing to their https://www.twitch.tv/ or patreon as a way to monetize WoW UI development


# ***-- 5. -- JarUI now lives on https://github.com/247jar/JarUI AND https://wago.io/p/Jar***

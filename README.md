***This is [Jar](https://www.twitch.tv/tvJar)'s World of Warcraft User Interface repository.***

***Here, I provide EVERY SINGLE STEP that is needed from a fresh WoW install to having your whole UI set-up to a state that allows for heading over to actual gameplay. The main purpose is to enable EVERYONE to learn about most crucial aspect about WoW UI, including:***
- [***-- 0. -- The WoW install process***](#---0----the-wow-install-process)
- [***-- 1. -- UI manipulation through local files***](#---1----ui-manipulation-through-local-files)
- [***-- 2. -- Managing ALL addons & simple update process***](#---2----managing-all-addons--simple-update-process)
- [***-- 3. -- Getting & sharing addon profiles***](#---3----getting--sharing-addon-profiles)
- [***-- 4. -- Popular Discords for fancy WoW UIs***](#---4----popular-discords-for-fancy-wow-uis)
- [***-- 5. -- External software***](#---5----external-software)
- [***-- 6. -- More about Jar***](#---6----more-about-jar)


# ***-- 0. -- The WoW install process***

### - 0.0 -- IMPORTANT WoW UI BACKUP!
DISCLAIMER: If you already have customizations inside WoW, these are the folders you need to backup: 
- ``D:\Battlenet\World of Warcraft\_retail_\Fonts`` -- global font replacements live here
- ``D:\Battlenet\World of Warcraft\_retail_\Interface`` -- ALL the WoW Interface data resources live here, e.g. addon installs, extra media, AND these texture replacements (icons, panels, etc.)
- ``D:\Battlenet\World of Warcraft\_retail_\Screenshots`` -- all YOUR screenshots you have taken over the years!!! These do NOT get cloud-backup through Blizzard!!!
- ``D:\Battlenet\World of Warcraft\_retail_\WTF`` -- HERE is where all your customizations live. ALL the config files for ALL the addons AND account data...


### - 0.1 -- WoW installation

To start off the WoW install, go to: https://www.blizzard.com/en-us/apps/battle.net/desktop
Within Battle.net install World of Warcraft. This will result in creating an install folder structure like 
- ``D:\Battlenet\World of Warcraft``
- The most recent WoW expansion Dragonflight is called the "Retail" version of the game - ther are older versions, like WoW Classic or Wrath Classic for past expansions.
- So for Dragonflight, the WoW install folder lives in: ``D:\Battlenet\World of Warcraft\_retail_``
- Within Battle.net, click on "Play" having "World of Warcraft" selected. 


### - 0.2 -- Ingame default System settings (audio, graphics settings, network)
At character select, we can already make first customizations - go to bottom-left Menu > System: 
- Audio: Master Volume 10%, Music+Effects+Dialog 20%, Ambience 0%. Everything ticked, except Error Speech!
- Graphics: Vertical Sync: Disabled, Low Latency Mode: Built-in, 
-- Graphics Quality: Base: Shadow Quality: Fair, Liquid: Good, Particle Density: Fair, rest use High, Spell Density: Most, Projected Textures: Enabled!, View Distance + Environment Detail + Ground Clutter: 7, 
-- Graphics Quality: Tick Raid Graphics Quality: Shadow Quality: Fair, Liquid: Good, Particle Density: Fair, SSAO: Disabled, Depth Effects: Disabled, Compute Effects: Disabled, Spell Density: Most, Projected Textures: Enabled!, View Distance: 7, Environment Detail + Ground Clutter: 1, 
- Graphics, Advanced: Triple Buffering: Untick, Texture Filtering: 8x, Ray Traced Shadows: Disabled, VRS Mode: Stamdard, Target FPS: Untick, Gamma: 1.2
- Network: Advanced Combat Logging: Tick / Enable!


Now login with a character! This will create first files in your ``D:\Battlenet\World of Warcraft\_retail_\WTF``


### - 0.3 -- Ingame default menu options (Gameplay settings)
- Controls: Mouse: Mouse Look Speed: 1

Now restart the game to make all the graphics settings changes go live. 

--- ingame default menu options -> will live on a video. maybe youtube. maybe a twitch clip. (interface settings, graphics settings, Advanced Combat Logging enabled!)
- TODO: but lives at https://www.twitch.tv/videos/1812917539?t=1h19m20s


# ***-- 1. -- UI manipulation through local files***


### - 1.1 Global Fonts
TODO: share the default font replacements - note: I use Expressway
- Inside ``D:\Battlenet\World of Warcraft\_retail_\Fonts`` we want to place ``.tff`` font files that will replace that named font globally inside WoW.
- I like to use **Expressway** for my global font for everything. So get my Fonts folder zipped up at https://github.com/247jar/JarUI/blob/main/Fonts.zip
- Unzip this ``Fonts.zip`` into ``D:\Battlenet\World of Warcraft\_retail_`` - this will then result in having ``D:\Battlenet\World of Warcraft\_retail_\Fonts``.


### - 1.2 INTERFACE folder - VERY PERFORMANT because it's only texture replacements!


Texture replacement packs (BIG topic, lots of work here)
- https://www.tukui.org/addons.php?id=202 for login screen & ingame Blizzard panels!!! (I use Grey > Transparent) 
-- unzip this ``elvui_login_screen_and_character_select.zip`` in your Downloads folder for now. This will unpack folders, we use: ``Retail > Grey > Transparent``. Place ALL contents (folders) from here into ``D:\Battlenet\World of Warcraft\_retail_\Interface`` -- NOT into that ``AddOns`` folder!!!


- https://www.tukui.org/forum/viewtopic.php?p=45464#p45464 use *No border with low background* for chat bubbles specifically. 
-- unzip https://github.com/247jar/JarUI/blob/main/no%20border%20-%20low%20background.zip and copy these 2x .BLP files ``ChatBubble.BLP`` and ``ChatBubbleVertical.BLP`` into ``D:\Battlenet\World of Warcraft\_retail_\Interface\Tooltips``
-- but now delete/move the existing chatbubble mods from ``D:\Battlenet\World of Warcraft\_retail_\Interface\Tooltips`` called ``ChatBubbleVertical.tga`` and ``ChatBubble.tga``


- Default Icon replacement packs for 1px border squared icons everywhere (no more skinning!) 
-- Go to: https://github.com/AcidWeb/Clean-Icons-Mechagnome-Edition
-- On the right side, download latest Release ``.zip`` - around 1GB file size!
-- extract that ``CleanIcons-MechagnomeEdition-10.1.0.49407-V4-1.zip`` and copy all contents into ``D:\Battlenet\World of Warcraft\_retail_\Interface``


### - 1.3 chat tabs / channels +++ Edit Mode scaling (maybe mention my UI Scale WA) note: start referring to JarUI
-- TODO: FOR every character go to ```WTF\Account\%ACCOUNT_ID%\SavedVariables``` and PASTE INSIDE THE FILE, DO NOT REPLACE EXISTING FILE BECAUE OF HASHING from: https://github.com/247jar/JarUI/blob/main/chat-cache.txt
-- for example: ``D:\Battlenet\World of Warcraft\_retail_\WTF\Account\137037127#1\Tarren Mill\Jarpd\chat-cache.txt``


----
# ***-- 2. -- Managing ALL addons & simple update process***


### - 2.1 ***I recommend WowUp.io with CurseForge to keep all addons updated with just 1 click - yes, including ElvUI: ``https://wowup.io/``***

- Inside the WowUp.io app, look at top right hand corner, next to "Check Updates", click on the vertical menu dots and import this String: https://github.com/247jar/JarUI/blob/main/WowUpio_CF_string.txt
-- This is install ALL addons (including ElvUI) that I use directly.


### - 2.2 ALL the addons that I currently use and are well maintained in Dragonflight:


- `AdiBags` (is my bag addon of choice because ***C A T E G O R I E S***)
-- Position & size: Scale 90%, Max bag height 42%
- `AdvancedInterfaceOptions` (offers a nice ingame CVAR browser + lowlevel interface options)
-- CameraDistanceMaxZoomFactor 2.6
- `Angry Keystones` (for displaying weekly affix schedule in the M+ panel)
- `BetterCharacterPanel` (for character panel: to display Item Level *and* Enchant, Socket info per equipped item *and* on Inspect frame too!)
-- TODO: not sure if I made adjustments or in `DejaCharacterStats` !!
- `BigWigs Bossmods` (the boss timer addon with the fastest updates) + ``BigWigs_Voice`` + ``LittleWigs`` (***TODO: SHARE PROFILES***)
-- download https://github.com/247jar/JarUI/blob/main/BigWigs.lua into ```WTF\Account\%ACCOUNT_ID%\SavedVariables```
-- TODO BEFORE RESET: test out making a new BigWigs profile on different Account.... to make sure we got ALL of the settings!!!!!!!!!
- `BlizzMove` (to actually be allowed to move ***all Blizzard panels***, *yes even the Exit Game menu*)
-- Global Config: 2x Remember permanently
- `BtWQuests` (TODO: maybe if u wanna complete all the questlines)
- `BugGrabber` and `BugSack` (as LUA debug tools for all WoW addons)
- `Can I Mog It?` (to keep track of transmogs)
- `DejaCharacterStats` (for character panel: to see Equipped Item Level / Max Item Level for LFG)
-- download https://github.com/247jar/JarUI/blob/main/DejaCharacterStats.lua into ```WTF\Account\%ACCOUNT_ID%\SavedVariables```
- `Details! Damage Meter` (***TODO: SHARE PROFILE***)
-- 1. ingame in Details! "Options", go to "Profiles" and "Import Profile" by pasting this String: https://github.com/247jar/JarUI/blob/main/Details_profile.txt 
-- 2. ON EVERY CHARACTER SWAP TO JarUI profile within Details!'s profile select
- `Echo Raid Tools` (adds a icon for guild Echo's WeakAuras to import ingame in the adventure guide)
- `ElvUI` (THE complete UI overhaul, well-maintained, huge community, tons of profiles to test out on https://wago.io/)
-- for JarUI import ALL profiles from this collection: https://wago.io/lw05cBLC4
- `FPS-MS-Tracker` (to display a tiny, *class-colored* fps and ms counter on the bottom left-hand corner)
- `HandyNotes` (adds icons to the map, can be expanded through lots of plugins / other HandyNotes - Addons)
-- **uses character specific settings by default !!! careful about committing to profile changes**
- `LS: Glass` (to have ***nice*** chat message animations and tab glow)
- ``Method Raid Tools`` (for raid CD tracking ***TODO: SHARE PROFILE***)
-- ingame in Method Raid Tools got to "Profiles" and "Import profile" by pasting this String: https://github.com/247jar/JarUI/blob/main/Method_Raid_Tools.txt
- ``Mythic Dungeon Tools`` (to edit, import & share M+ dungeon routes ***TODO: EXPLAIN M+ LIFE - keystone.guru, raider.io weekly route, getting MDT strings from streamers, big pushers.... all that fun***)
- `Narcissus` (to have a very modern, gorgeous character display)
- `OPie` (for a selection ring around your mouse cursor)
-- set up Alt-Q for Target Markers ++ and Alt-E for World Markers
- `OmniCD - Party Cooldown Tracker` (for party cooldown + interrupts tracking -- ***TODO: SHARE PROFILE***)
-- download https://github.com/247jar/JarUI/blob/main/OmniCD.lua into ```WTF\Account\%ACCOUNT_ID%\SavedVariables```
- `Outfitter (Equipment Manager - Nulian's Fixed)` (the new Dragonflight version - to click on equipped item and immediately see replacement options inside character panel!)
-- ingame open up the charactger panel, on the top right hand corner click on the gray cloth chest icon (this open Outfitter settings) - go to bottom tab "Options" - and untick all of the 4 default ticks.
- `Paragon Reputation` (for old Legion reputation paragon chests)
- `Pawn` (simplistic item upgrade hints in the tooltip)
- `Plater Nameplates` (THE addon for WoW nameplates. ***EXPLAIN: go to wago.io to import Plater profiles - mention Jundies, Naowh Twitch sub, etc.***)
-- I use Jundies' well-maintained and free profile: https://wago.io/ak3iS95aa
-- for every character swap to the desirec profile in the settings.
- `Prat 3.0` (to modify chat text)
-- go to "/prat" > tab "Chat Formatting" > select "Timestamps" and use the HH:MM (24-hour) formatting
- `Premade Groups Filter` (to have more functionality in filtering through the LFG queue)
- `Project Azilroka` (***only use Enhanced Friends List***... disable all other modules!)
-- go to ElvUI settings with "/ec" > bottom tab "ProjectAzilroka": DISABLE every module, except Enhanced Friends List
- `RCLootCouncil` (to ingame manage loot distribution... ***maybeeee explain Droptimizer, WoWaudit, blekfjbnsejikf bnsikjf nsuikdf b***)
- `Raider.IO` (to display https://raider.io/ scores, past keys in tooltip in LFG)
- `RareScanner` (to get alerts of rares and more map options like more map icons, dungeon/raid entrances)
-- in order to get some quiet from rare alerts, just go to AddOns> RareScanner > Zone filtesr > and just "Toggle filters" for Dragon Isles - so when you're chilling in Valdrakken, there won't be alerts. You can re-Toggle filters, or just actually join a rare farm group for that purpose. Who even needs those alerts max-lvl?
- `SavedInstances` (to get an overview list of all relevant alts with their info, like lockout, weeklies, M+ keys etc.)
- `SharedMedia` (offers a framework to share addon resources, like textures, sounds, etc.)
- `SharedMedia_Causese` (most https://wago.io imports rely on this SharedMedia by Causese for alerts etc.)
- `Simulationcraft` (to type "/simc" ingame for a quick character data sheet to paste into https://www.raidbots.com/simbot/droptimizer )
- `Talent Loadout Ex` (to save many more talent tree Strings)
-- download https://github.com/247jar/JarUI/blob/main/TalentLoadoutsEx.lua into ```WTF\Account\%ACCOUNT_ID%\SavedVariables```
- `Talent Tree Tweaks | Dragonflight` (to make the talents panel smaller, transparent etc. - and more by Numedain)
-- download https://github.com/247jar/JarUI/blob/main/TalentTreeTweaks.lua into ```WTF\Account\%ACCOUNT_ID%\SavedVariables```
- `Talent Tree Viewer (calculator) | Dragonflight` (to see other classes' talent trees, by Numedain)
- `TeleportCloak` (reliably & automatically re-equipps previous cloak after using any Teleport Cloak in the game)
- `TomTom` (THE addon for questing, offers an arrow, coordinates, /-commands)
- `WarpDeplete` (THE most complete Mythic+ dungeon timer)
-- download https://github.com/247jar/JarUI/blob/main/WarpDeplete.lua into ```WTF\Account\%ACCOUNT_ID%\SavedVariables``` to get the Default profile
- ``WeakAuras`` (THE framework to add UI work shared on https://wago.io )
-- See [section about Recommended WeakAuras](#--32----recommended-weakauras)
- `World Quests List` (THE best world quest addon, displays listing of ALL available WQs next to the world map)


# - 2.3 quickly import global Account settings:
- inside ``D:\Battlenet\World of Warcraft\_retail_\WTF\Account\%ACCOUNT_ID%\SavedVariables\`` are all the global config files, usually ``%ADDON_NAME%.lua``.

These addons we will copy+paste straight from my git into their accountwide/global ``.lua`` config files:
- `BigWigs Bossmods` - https://github.com/247jar/JarUI/blob/main/BigWigs.lua
- `DejaCharacterStats` - https://github.com/247jar/JarUI/blob/main/DejaCharacterStats.lua
- `OmniCD - Party Cooldown Tracker` - https://github.com/247jar/JarUI/blob/main/OmniCD.lua
- `Talent Loadout Ex` - https://github.com/247jar/JarUI/blob/main/TalentLoadoutsEx.lua
- `Talent Tree Tweaks | Dragonflight` - https://github.com/247jar/JarUI/blob/main/TalentTreeTweaks.lua
- `WarpDeplete` - https://github.com/247jar/JarUI/blob/main/WarpDeplete.lua


- `Details! Damage Meter` (***TODO: SHARE PROFILE***)
-- 1. ingame in Details! "Options", go to "Profiles" and "Import Profile" by pasting this String: https://github.com/247jar/JarUI/blob/main/Details_profile.txt - save as "JarUI" and always swap to this profile on all new characters.

- ``Method Raid Tools`` (for raid CD tracking ***TODO: SHARE PROFILE***)
-- ingame in Method Raid Tools got to "Profiles" and "Import profile" by pasting this String: https://github.com/247jar/JarUI/blob/main/Method_Raid_Tools.txt - import with "Rewrite current" "Default" profile, so it applies to all characters now.


----
# ***-- 3. -- Getting & sharing addon profiles***

- https://wago.io/ biggest platform to share String / text based profiles for most popular addons (WeakAuras, Plater, ElvUI, Blizzard Edit Mode)


### - 3.1 -- ***all the addon profiles*** TODO: complete list of addons and share their profiles on github

share each individual addon profile.... THAT CANNOT BE SHARED THROUGH https://wago.io ON ***https://github.com/247jar/JarUI***

- ``Edit Mode`` (Blizzard Default UI) - https://wago.io/36N3iSP-P


### - 3.2 -- ***Recommended WeakAuras***
- ``WeakAuras`` (THE framework to add UI work shared on https://wago.io ) 

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


### - 3.3 -- ***ElvUI wago.io collection***: https://wago.io/lw05cBLC4

- we use ***Prat 3.0*** for chat customization.
- we use ***Plater*** for nameplates.


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


### - 3.4 -- ***Plater from wago.io***
I recommend Jundies Plater profile: https://wago.io/ak3iS95aa


# ***-- 4. -- Popular Discords for fancy WoW UIs***
naowh, atrocity, tukui, etc...........
TODO collect all of them
explain subbing to their https://www.twitch.tv/ or patreon as a way to monetize WoW UI development



# ***-- 5. -- External software***

### - 5.1 -- ***Warcraft Logs Uploader***
- https://www.warcraftlogs.com/client/download
- enable auto combat logging in BigWigs BossTimer - in Pull section
--> NEEDS A BIGWIGS PULLTIMER!!! NOT A DBM OR DEFAULT BLIZZARD PULL TIMER!!! "/pull 15" with BigWigs!!!


### - 5.2 -- 


# ***-- 6. -- More about Jar***

- JarUI now lives on https://github.com/247jar/JarUI AND https://wago.io/p/Jar (ElvUI, WeakAuras, Plater, Edit Mode, OPie***



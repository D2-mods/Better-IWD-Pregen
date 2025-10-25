Better IWD Pregen
GitHub: https://github.com/D2-mods/Better-IWD-Pregen
Download: https://github.com/D2-mods/Better-IWD-Pregen/releases
Supports: classic and EE versions of BG1, BG2, IWD1, and IWD2 (including EET/BGT/IWD2EE)

--

A minimalist script and tweak pack for Infinity Engine games. This mod was started as an attempt to make an improved version of the IWD Pregen party AI script from Icewind Dale: Enhanced Edition.

- See GitHub page for additional info on scripts and tweaks.
- This mod supports any mods using the engines of supported games.
- Older EEs that don't support v2.0+ features are treated the same as original BG2 engine.

--

Recent updates:
- added PSTEE support for several tweaks
- added Misc spell tweaks component (see GitHub readme)
- added "Make items stackable to 999" (weapons and magic items optional)
- added Shapeshifts can talk (EEs, BG2)

PSTEE note: Generalized Biffing is not required for PSTEE. The bag from this mod will not reset when doing the Modron Maze (it is biffed automatically when installing). However, it's still recommended to install Generalized Biffing (option 2 - biff all) if using any other mods that edit areas or store files.

--

Updated IWD Starting items tweak (summary of major points):
- now supports IWD1, IWD2, IWD:EE, IWD-in-BG2, IWD2:EE, Classic Adventures, Tutu, BGEE/EET/BGT (BG1 part only).
- Scripting is now done for all PCs simultaneously instead of one at a time.
- EEs/BG2 engine: autoequip option now accounts for mastery and specialization (up to 3+).
- Autoequip option is now compatible with proficiency overhauls, install this mod after anything that changes proficiencies.
- IWDEE: fixed the issue that could pause the scripting when starting a new game. (note: fix is only for this mod. If you see this issue with other mods, saving and reloading should fix it.)
- better reliability on original BG2 engine (i.e. fixed issues that could prevent gaining items).
- Bag option: adjusted item order, added a couple items that were previously intentionally left out (ex. heavy crossbow).
- accounts for some additional mod items if detected (rr shortbows, project javelin).
- added journal entry, bug fixes, other improvements (better weapon mix for IWD1/IWD2, etc.).


==================================================
Components
==================================================
Script components:
1. Better IWD Pregen
2. Better AI for Call Woodland Beings (EEs, BG2)
3. Auto-assign script to new characters

Tweak components:
1. Adjust enemy damage at higher difficulties (IWD1, IWD2)
2. Add or remove Avarine Decanter (IWD2)
3. Unnerf Animate Dead (IWD2)
4. Shapeshift movement bonuses bypass Free Action (EEs, BG2)
5. Increase movement speed of IWD shapeshifts (IWD1, IWDEE)
6. Shapeshifts can talk (EEs, BG2)
7. Starting items tweak (all IWD games, BGEE/EET/BGT, Classic Adventures)
	- Option 1: Autoequip or added to inventory
	- Option 2: Weapon Sack (has at least one of each weapon type)
8. Start with a Bag of Holding (classic and EEs)
9. All classes get full HP bonuses from Constitution (classic and EEs)
10. Make items stackable to 999 (classic and EEs)
11. Reduce delay for Sneak Attacks + uncap Crippling Strike (EEs)
12. Salamander auras hit only enemies of the caster (IWDEE)
13. Misc spell tweaks (classic and EEs)
	- Damage party friendly (relative to caster)
	- Hit stun on damage (1 second)
	- No mage school restrictions
14. Allow Minsc to use his Berserk ability at will (BG games)
15. Patch visuals for shortbows (IWDEE) or scimitars (IWD-in-BG2)
16. Remove alignment restrictions for classes (classic and EEs)
17. Prevent paladins and rangers falling at low rep (EEs)
18. Max summons and traps (EEs)

--

Additional info:
- All components can be installed independently and in any order, except for auto-assigning the script.
- All components should be safe to install at end of order. If another mod says to install last, you can try it both ways.
- If using tweaks from other mods that do similar things, whichever is installed last will usually be used.
- All tweaks have at least 2 subcomponents. i.e. if you say to "install all components", it won't automatically install any tweaks.

Notes on a few mods:
- IWD2EE: This mod is safe to install before or after the IWD2EE compatibility patch.
- EET_end: This mod is safe to install before or after EET_end. (basically, if SCS or another mod says to install after EET_end, you can install this mod after as well)


==================================================
Script Compatibility (v4.0+)
==================================================
EEs: BG:EE, BG2:EE, IWD:EE, EET (tested on v2.5/v2.6)
Classic: BG1, BG2, IWD1, IWD2 (tested with GOG versions)

Also compatible with any BG2 conversion mods (ex. BGT or Classic Adventures).

Classic BG2 engine:
TobEx (v26/v28): Compatibility issues should be fixed (v3.7 and later).
TobEx Afterlife: Use v29.10 or later. (http://www.shsforums.net/files/file/1274-tobex-afterlife)
Improved GUI mod: Use v5.1 or later. (http://www.shsforums.net/files/file/1265-bg2-improved-gui)

NOTE: I'm not 100% sure the scripts work with expansionless versions of the classic games.


==================================================
Script Description (adjusted for each game)
==================================================
The character will auto-attack when enemies are in range*, but will not attack if under the effects of invisibility or sanctuary, or if using Stealth, Bard Song, Turn Undead, or Shamanic Dance. If not in auto-attack range, a character with skill points will search for traps or illusions, but not if using Stealth, Bard Song, Turn Undead, or Shamanic Dance. (<script>)

*Melee auto-attack range is dependent on class (see readme for full breakdown).

Cooldown mode: Reduces melee aggro range to 5 feet. Press the B key to enter for 5 rounds, or the E key to deactivate instantly.


==================================================
Tools/Coding
==================================================
Custom Functions:
- CD_LEVEL_SELECT-O-MATIC, by CamDawg (https://www.gibberlings3.net/forums/topic/28835-toss-your-semi-useful-weidu-macros-here/#comment-254220)
- 2DA_MISSING_COLS - by K4thos (https://github.com/K4thos/IE-code-repository)

Tools and Resources used:
- WeiDU (https://github.com/WeiDUorg/weidu)
- NearInfinity (https://github.com/Argent77/NearInfinity)
- Notepad++ (https://notepad-plus-plus.org/)
- Git Bash (https://git-scm.com/downloads)
- WeiDU Mod Packager (https://github.com/InfinityTools/WeiduModPackager)
- IESDP (https://gibberlings3.github.io/iesdp/main.htm)
- WeiDU readme (https://weidu.org/~thebigg/README-WeiDU.html)
- LibIconv for Windows (http://gnuwin32.sourceforge.net/packages/libiconv.htm)

Used for older releases (replaced by WeiDU Mod Packager):
- Infinity Auto Packager (https://github.com/InfinityTools/InfinityAutoPackager)
- 7-Zip (https://www.7-zip.org/)

TobEx.dll:
- Patched DLL file was made by Insomniator and used with permission.
- http://www.shsforums.net/topic/61135-question-about-featurebug-change-to-the-noaction-script-action/#entry612382

IWD2 exe patch:
- Patch for the enemy damage component was written by Bubb and used with permission.
- https://www.gibberlings3.net/forums/topic/35670-adjusting-difficulty-levels-iwd2/#comment-311240


==================================================
Updates
==================================================
v7.27 (v8.0)
- added more installer feedback when scanning files.
- fixed compatibility issues with Tutu/EasyTutu mod. (some strange design decisions were breaking things that work in BG2/BGT/Classic Adventures)
- updated Stackable items tweak: it wasn't scanning .bcs files properly, most relevant scripting is in .dlg files so this was relatively minor.
- Auto-assign script: now fixes SCRLEV.ids for iwd games again. This reverts change from v7.24 that removed the fix.
- Stackable items tweak (non-EE games): fixed installer errors or warnings due to trying to decompile bsd scripts. These were popping up after the improved .bcs scanning.
- IWD2EE note: fixed Starting items tweak being buggy with IWD2EE due to recent updates.
- SoD note: if Starting items tweak is installed, this will make it so characters pregenerated at level 1 from the BG1 part gain SoD starting items when imported into SoD. (in the unmodded game, they are treated as already equipped)
- Starting items tweak: accounts for some additional mod items if detected (rr shortbows, project javelin).
- Spell damage tweaks: added additional checks for RoyalProtector's mods to avoid patching subspells used for on-hit damage.
- Stackable items tweak should install much faster after SCS AI components now (tested with v35.21).

v7.26
fixes for IWD/BG1 Starting items tweak:
- IWD2: fixed rangers possibly getting a bow paired with bolts instead of arrows.
- BGEE/EET/BGT: it wasn't giving weapons or ammo for monks (requires a staff and monks don't start with one in these games).
- BGEE/EET/BGT: Weapon Sack option did not include a staff in the bag.
- IWD1/IWD2: fixed an issue (caused by recent update, not sure which one) that made it not give weapons or ammo when importing a character with an empty inventory.
- fixed issues for some games when importing a CHR that already had a quarterstaff.
- better start up speed for nonglobal mode (settings.ini), still slower than global mode but faster than before.
- IWD2: weapon sack mode now removes starting staff and includes 1 in the bag (like all except iwd1).
- iwdee/iwdification, added rng for greataxe or battle axe if you take axe prof with no weapon styles.
- bgt: recently added quarterstaff checks were conflicting with bgt scripting. (was making bgt not give a melee weapon at the start of bg1)
- iwd2: fixed minor but annoying issue where melee weapon would sometimes not get moved to quickslot if the imported CHR did not have a quarterstaff already.

v7.25
fixes for IWD/BG1 Starting items tweak:
- EEs/BG2 engine: fixed edge case issue that could prevent a character with 11 or 12 STR from gaining a morning star if taking the flail/morning star prof.
- fixed solo PC journal entry for BGT/Tutu/Classic Adventures. It was adding the IWD entry when starting BG1 (written as if you just arrived).
- EEs/BG2 engine: fixed issue (wrong variable) that made the class-specific blocks not account for mastery/specialization.
- EET/BGT note: the default "global" mode in settings.ini now mostly uses the area script instead of baldur.bcs. Other games still use baldur.bcs because it starts up faster on a new game. NOTE: summoning invisible CREs is still done by global script (combo of CRE + global/area script is fastest).
- BGT: it was using an unset variable for something (made part of scripting be skipped).
- BGT: scripting oversight was making it give the starting robe when starting a new game in BG2.

v7.24
- Starting items tweak now usable with BG1 games. Compatible with BGEE, EET, and BGT (also accounts for Tutu but haven't tested with it).
- "Auto-assign script" component no longer fixes SCRLEV.ids for iwd1/iwd2. (info: The table is wrong in both games so the IDS names will be wrong. This mod works around it by using the script number directly.)
- Starting items tweak (autoequip): Minor fix for last update (compat with prof overhauls). Some classes could still get a weapon they couldn't use (ex. a thief or monk with "Blunt" prof would not get a club). Now if a proficiency includes usable and unusable weapon types, they should always get a weapon usable for the class. (note: Some edge cases might get through, ie kits with weird restrictions.)
- added a settings.ini file that lets you reduce global scripting with the IWD/BG1 Starting items component. This was really made for myself to test scripting methods but I left it in the release version if you want to use it.
- the Worn Garment item from the Starting items component can now be purchased for cheap if you want extras for whatever reason. It's added to one store in each game in unlimited quantities.

v7.23
IWD Starting items tweak update (autoequip):
- now compatible with proficiency revisions/overhauls, including "skills" mods that add non-weapon profs. This mod needs to be installed after any mod that changes proficiency categories. This is so it knows what prof number to use for each weapon. (This mod doesn't use a predetermined number, it scans the info for each weapon type at install time.)
- can now start with ninjato, wakizashi, or morning star (previously, these were left out). Chance of starting with these is smaller than scimitar or flail. This will also adjust for prof revisions. Note that a druid will never start with these over scimitar (it can't use them).
- IWDEE/BG2 engine: Autoequip option now also checks for mastery and specialization. Previously it was only checking if you had any points at all in the weapon. Weapons with more points have higher priority (up to 3+).
- iwd1 (classic): updated the weapon mix for the autoequip option. Player1 will always start with 1 bladed weapon, 1 blunt weapon, and 1 ranged weapon (all randomized). Each additional PC adds 2 more weapons taken from arbitrary groupings (blade, blunt, heavy, ranged). It has to be randomizaed because you can't check profs in this game but it should (hopefully) give a better mix than before.
- added a couple Flaming Oils, these are the weak 2d8 damage ones (not per character, 2 total with either install option).
- also added a couple Elven healing wines (2d8 healing). Both potions are cheaper than normal so they won't sell for much.
- added Strength checks, fixes an issue where if using a mod that combines weapon types, it could give you a weapon you didn't have the STR for.

v7.22
IWD Starting items tweak notes:
- IWDEE: fixed issue where scripting would sometimes get interrupted at the start of IWDEE.
- IWDEE: fixed an issue where if you clicked too fast and moved before the starting dialogue, the character would not get the starting robe.
- IWDEE: fixed a possible issue with the bag option where the starting quarterstaff wasn't always being removed.
- BG2 engine (Classic Adventures, IWD-in-BG2): fixed possible issues when starting with a single pregenerated character (sometimes failed to add weapons for various reasons).
- Bag option: ammo stack sizes now adjusted by party size (20, 40, 60, or 80).
- Journal entry now added as confirmation that items were added.
- Worn Garment (starting armor) resists increased from +3% to +5%. (no change for IWD2)
- Major changes internally with install files and script compiling.
- Autoequip option: scripting now runs for all party members simultaneously instead of one at a time.
- IWD2 (autoequip): adjusted possible starting weapons for some classes, every type is possible from at least 2 classes now. (note: bastard sword only available from bag option)
- IWD-in-BG2: fixed greataxe being bugged (turns into pile of gold). NOTE: only the ones given by this component are fixed. (bug is only with regular greataxe, so it's not a huge issue)
- Bag option: Adjusted item order, added some missing items (composite bow, heavy crossbow). For IWD2 the bag no longer has masterwork handaxe (it already has 3 other types of axes).

v7.21
- added missing WeiDU LABELs for a component, i.e. so it can be detected by Project Infinity.
- EEs: Installing "Shapeshift movement bonuses bypass Free Action" (both options) will now also check movement rates on IWDification shapeshifts. The animals will move similar speed to BG2 animals.

v7.20
- Added component: Shapeshifts can talk (EEs, BG2). This does not allow spellcasting, but you can talk to NPCs, merchants, etc.
- iwdee: faster shapeshifts tweak now also increases boring beetle and elemental speeds. They are still slightly slower than natural form, but fast enough to be usable out of combat.
- Shapeshift movement tweaks now account for EE fixpack changes.
- Updated "Shapeshift movement bonuses bypass Free Action": This now also checks haste. Some mods give shapeshifts haste instead of a movement bonus to increase walking speeds. Also, this is now installable on classic BG2. This also now accounts for mod abilities.

v7.19
- Added component: Max summons and traps (EE-only). Has 6 options with various max summon or celestial numbers. Traps are always set to 999 with any option.
- SoD + "Items stackable to 999": fixed a random treasure (in BD0130 container 33) becoming 20 items instead of 1 item.
- iwdee + EE fixpack: fixed a compat issue with the salamander auras tweak. The party friendly Cloudburst options weren't blocking the lightning damage if EEFP was installed.

v7.18
IWD "Start with items" notes:
- now also installable on Classic Adventures. Also made scripting on original BG2 engine more reliable (other than CA, this is only relevant for IWD-in-BG2).
- fixed possible mod conflict with "Eliminate race/class restrictions" from Talents of Faerun mod. The ToF component uses a wrong setting for nonhuman monk avatars, which causes the avatar to disappear permanently if equipping an armor (either on equip or unequip), i.e. the starting robe would previously make the avatar disappear.
- this will also fix a couple possible issues with half-orc monk avatars, also caused by ToF (missing paperdoll, uses human appearance instead of half-orc).

v7.17
- Script components no longer fail to install on older EE versions. EEs that don't support v2.0+ opcodes will have the same scripting as original BG2 engine.
- Minsc rage component now only uses EE version of tweak for EE v2.0+. Older EEs will be the same as original BG2 engine (ability is usable again only after duration ends).
- Spell tweaks component no longer crashes EE versions older than v2.0.

v7.16
"Items stackable to 999" notes:
- iwd2: fixed an issue that made it so items in stores (if 2+ in stock) were purchased in the full stack, instead of individually. (note: selling stackables in IWD2 may increase stack size instead of store quantity. This is just how the engine works. This is only an issue if you sold something and wanted to buy it back.)
- bg1/iwd1 (classic): fixed an issue that made it not work for many items. Items in these games need an ability header to be stackable, so the installer now adds an empty header for items that don't already have one.
- installer won't give DLG-related weidu warnings anymore for BG1, IWD2, IWD-in-BG2, or Classic Adventures.

"Give party starting items" notes:
- iwd1 (classic): improved scripting. Previously, you sometimes had to open/close the inventory before items were added. They should be added without having to do this now.
- iwdee: It now always gives the starting robe if the character does not start with a usable armor, even if no other part of the script triggers (ex. starting a new game in HoW).
- iwd1/iwd2 (classic): every PC always starts with the starting robe if they don't already have it.
- Autoequip option: the scripting now runs once for all 6 PC slots, whether or not they are filled. (i.e. a character that joins later will not have the scripting run for it)

v7.15
- Bag component: fixed harmless NI warning with EET when looking at AR0602.bcs (BG2 starting area).
- IWD2: damage tweak now aborted during install if iwd2.exe isn't detected.
- IWD1 (classic): added component note for damage tweak that it also disables XP bonuses. Damage and XP bonuses cannot be toggled separately for original IWD1.
- updated Stackable items component: it now also scans all DLG/BCS files for scripting that takes items from the party. Only items changed from nonstackable to stackable by this tweak are checked. Any scripting that could possibly take a whole stack of items will be changed to have a single item taken. (note: for original BG1 and IWD1, a full stack is still taken.)
- bg2 (classic): fixed web possibly being party friendly with Damage party friendly tweak. (an unused item in the base game was causing the web projectile to be flagged for patching)
- bg1 (classic): Stackable items component now fixes some bg1 DLG errors to prevent weidu warning messages. Only files that could potentially affect this mod's install are fixed.

v7.14
- update to "Start with bag" component: Adjusted buy and sell markups for the gold-exchanging bag option (EE-only). Numbers are also slightly different for IWDEE/PSTEE. The main change is that buy back prices if you need an item back aren't as insanely marked up now (was at 180%, now at 130% or 140%, depending on game).

v7.13
- pstee: added support for "Start with bag of holding" component.
- NOTE: Generalized Biffing is not required. Bag does not reset when doing Modron Maze.

v7.12
Bug fixes for "stackable to 999" component:
- Option 4 now skips weapons with charges (possible bugs, UI issues).
- Any item with per day charges is now skipped (EEs: putting drained item on a not-drained item makes the drained item disappear, if stackable).
- Installer now checks items in a bag/container. Any item changed from nonstackable to stackable is set to 1 charge if it was at 0 charges before. This fixes bugs caused by having 0 charge stackables in bags (underflow or drained/disappearing items).

v7.11
- added component: Make items stackable to 999. Has 4 options:
	- Option 1: Stackable or nonmagical, no weapons
	- Option 2: Stackable items only
	- Option 3: Stackable or nonmagical, with weapons
	- Option 4: All magical and nonmagical items (skips items with charges)
- items with charges are skipped if it can carry more than 1 charge (prevents stacking bug).
- critical or conversable items are always skipped.
- NOTE: It's safe to equip an item in a stack. Only 1 item in the stack is considered equipped.

v7.10
- Spell damage tweaks now working with IWD2EE mod ("Damage party friendly", "Hit stun on damage"). Specifically, the installer now accounts for the IWD2EE damage opcode (opcode 500 with "EXDAMAGE" function).
- IWD1/IWD2: "Damage party friendly" now working with Blade Barrier and Circle of Bones. A few other adjustments. (note: hardcoded effects or projectiles will still get through. If unsure, test if a spell hits PCs before using.)
- BG2 (classic): Better method for updating TobEx.dll if TobEx Afterlife/Improved GUI is detected (script component). The installer already accounted for these, but with the old way it was possible to miss detecting Improved GUI.
- PST/PSTEE: "full HP bonuses from Constitution" now installable.

v7.9
Spell tweaks updates:
- "Hit stun on damage" now skips repeating area damage (ex. Cloudkill). Similar mod spells are skipped if Secondary type is set to BATTLEGROUND.
- "Hit stun on damage" now skips counter/barrier spells (Fire Shield, Blade Barrier, etc.). Similar mod spells are skipped if Secondary type is set to any PROTECTIONS type.
- "Hit stun on damage" now skips beholder rays damage.
- "Party friendly damage" now catches more stuff in IWD2 (including some damage applied directly by projectiles or hardcoded effects).

v7.8
- new component: Misc spell tweaks (classic and EEs). This has 3 tweaks:
	- Damage party friendly (relative to caster)
	- Hit stun on damage (1 second)
	- No mage school restrictions
- Safe to install at end-of-order. Install after any mods that adds spells or items.
- It has multiple subcomponents. You can install all tweaks, just 1 tweak, or any combo of 2.
- The damage ones will also check item spells (wands, potions, etc.).
- See readme on GitHub for more info.

v7.7
- IWD2: Updated crash fix from last update ("Give party starting items" with G3 NPC mod). New version of NPC mod broke the previous fix, so it's been adjusted to work with both old and new versions of the mod.
- Fixed possible install error on Mac systems, caused by using text files without extensions.

v7.6
- Fixed possible mod conflict issues with "Start with bag of holding" component (scripting related).
- IWD2: Fixed a possible crash if using "Give party starting items" component and G3 IWD2 NPC mod.
- Alignment component: If skipping clerics/druids, the base fighter/druid multiclass will no longer be patched. (kits were already skipped, but base class was not)
- Minsc Berserk component: fixed possible issue in classic BG1 engine where Berserk ability could be lost permanently if delayed effects were canceled before applying. (if this happens now, ability should be regained after rest)

v7.5
- Script changes:
	- Slightly increased melee attack ranges.
	- Improved retargeting scripting (trolls, casters).
	- Powder Keg songs (from Workshop Kitpack) are now usable while invisible. Use v5.9 or later of Workshop Kitpack.
	- EEs: changed log text color (Cooldown mode hotkeys).
- Call Woodland Beings component:
	- Adjusted targeting scripting. Minimum 8 second cooldown between casts of status spells.
	- Adjusted triggers for "RunAway" and teleport actions.
	- AI can now cast Barkskin, Mass Cure, Entangle, or Summon Insects once each per combat encounter.
	- When the AI uses these spells, it doesn't require or consume any memorized spells.
	- Small increase to movement and casting speed.
	- Changes also apply to enemy summons (except move/cast speed).
- nymph script fixes:
	- Allied nymphs should no longer attack PCs if hit by accident (or if summoner is hit by a PC).
	- Fixed "marked" PC switching with Option 2 (patch existing script). Caused some weirdness with Dimension Door if the summoner died or left the map.

v7.4
- Fixed an issue that would cause the salamander tweak for IWDEE to fail at install, if a previous mod added SPL files with no headers to the override folder.
- Fixed an issue that made archers/beast masters still able to fall if using the "Prevent paladins and rangers falling" component.
- Can now choose to skip mod items for the shortbow patch for IWDEE. (modders might make weird items with intentionally different visuals than normal).
- Also fixed a potential issue with the shortbow patch. It could previously fail (not an error, just do nothing) if installed after a proficiencies overhaul on a non-English install of the game.

v7.3
- Added tweak for IWDEE: Salamander auras hit only enemies of the caster. Has multiple options. Can patch all salamander auras, or just the Avenger shapeshift (i.e. if you want enemy auras to still damage anyone). Can also optionally make Cloudburst party friendly.
- classic BG2: the tweak for Minsc's Berserk will now update the description if using the Improved GUI mod from Insomniator. Install this mod after Improved GUI. The description uses the same layout as Improved GUI, with duration changed to match the component.
- BGEE/BG2EE: Fixed issue (caused by v7.2 update) that made description for Minsc's Berserk always say 1 turn duration, even if setting to 5 rounds or 2 turns.
- Added more detailed component info to GitHub page.
- More improvements to install files.

v7.2
- IWD2/IWD2EE mod:
	- This mod is compatible with IWD2EE. Install this mod after IWD2EE.
	- 'Unnerf Animate Dead' will be skipped if IWD2EE 'Spell Revisions' is installed (it splits zombies and skeletons into separate spells, which include the stronger summons).
	- If using the 'Give party starting equipment' component, then also install this mod before the IWD2EE compatibility patch. It adds an effect to the 'Worn Garment' starting armor. Otherwise, I don't think it should matter.
- Removed component: Fixes for backstab-related 2DA files. Not really a fit for this mod.
- Fix/update for 'All classes get full HP bonuses from Constitution':
	- The '3e-style bonuses' option was only updating non-warriors. It will now apply to warrior classes. (Warning: Prism from BG1 will spawn dead if using '3e-style bonuses'.)
	- Added 3rd option: 'Mixed (use 3e-style at 10+, normal BG penalties at under 10)'.
	- Note that this component edits only the HP bonus. If you install this after another Con tweak, any changes to other Con effects will be kept.
- More options added for these components:
	- 'Remove alignment restrictions for classes': Now has multiple subcomponents, allowing to skip certain classes (paladins, clerics, monks, etc.).
	- 'Prevent paladins and rangers falling at low rep': Can now install for rangers only or paladins only.
- Minsc's Berserk tweak was using wrong description for '1 turn duration' option (it was saying 5 rounds).
- Internal installer improvements.

v7.1
- Fixes
	- d2scrp scripts: Removed a duplicated script block.
	- vanilla IWD Pregen script: Fixed an issue with bards modded to have Search skill.
- Revised d2scrp- script:
	- Same as standard script, except default mode is Cooldown.
	- E key will disable Cooldown mode for 30 seconds. B key reactivates it instantly.
	- Unlike v7.0, no script blocks are removed. Cooldown mode already disables certain actions.
- Expanded "Auto-assign script" component:
	- There are 3-4 options now, one for each script added or patched by this mod.
- Installer improvements + expanded weapon arrays handling.

v7.0
- Fix for "Auto-assign script" with classic BG1:
	- It was firing every time loading the game, due to using a local variable (which don't get saved in BG1).
	- I've changed it to use a Global variable. However, it won't run for every character.
	- It will now run once per party slot per playthrough (Player1, Player2, etc.).
- Changes for "Better IWD Pregen":
	- Main Script file renamed to d2scrp.BS (changed from iwdpgen.BS).
	- Added d2scrp-: Same as base script, except some retargeting actions are disabled.
	- Added d2scrp+: Same as base script, except calls for help are enabled.
	- IWDEE: Will patch the vanilla IWD Pregen script to include shaman abilities (basically what the v0.1 of this mod did).
	- BGEE/BG2EE/EET: Will also install the vanilla IWD Pregen script (with shaman added) as iwdpgen.BS.
	- Rewrote the install. Easier to edit or insert new script blocks.
- Changes for "Give party a Bag of Holding":
	- Improved scripting for adding the bag, based on work with the D2-Mira mod.
	- Option D (gold is exchanged) will now also add the bag if starting a new game in ToB. The other options won't give a bag in ToB because you already start with one.
	- All options now compatible with Black Pits 1 & 2.
- Changes for "Increase movement speed of IWD shapeshifts":
	- Can now install on classic IWD.
	- Will increase speed of all shapeshift forms (game only has the 6 Druid shapeshifts).
	- Wolf is faster than normal speed. Other forms are same speed or slower (but faster than unmodded).

v6.0
- Script update:
	- EEs: Any character with skill points in detecting traps or illusions will now have auto-Search enabled. Previously, the feature was only for specific classes.
- "Give party starting equipment" (auto-equip):
	- for IWD2 and IWD-in-BG2, it will now give a reminder in the dialogue box to update the quick weapon icons by saving/reloading or re-equipping weapons.
	- Increased ammo stacks given to 40 (was 20)
- "Give party starting equipment" (item bag):
	- will now have at least 1 of every weapon type (i.e. battle axe, greataxe, and throwing axe are 3 different weapons)
	- Increased ammo stacks given to 40 (was 20)
	- if Thrown Hammers mod is installed, 5 Throwing Hammers are added to the bag
- Fixed compatibility issues or install issues with a few other mods.
- Updated install files for several other components.
- Made some of the component info during install more descriptive (i.e. compatibility with other mods).
	- Related to this, also removed redundant components.
- Updated GitHub page with all the info from the Tweaks readme.

v5.0
- EEs: Fixed retargeting against enemy casters. Retargeting should work now if an enemy uses Protection From Magical Weapons, or similar, during the battle.
- Adjusted some attack actions in all scripts (classic and EEs).
- Bumped version to 5.0 because some actual scripting bugs were fixed for EEs and IWD2.

v4.5
- some backend changes
- CON bonus component now patches the file (won't change anything other than HP gains)

v4.4
- all tweaks really have at least 2 subcomponents now (missed a few in the v4.3)

v4.3
- All tweak components now have at least 2 subcomponents (even if just a simple "Yes" or "No")
- Added 2 components:
	- Remove alignment restrictions for classes (classic and EEs)
	- Paladins and Rangers do not fall at low rep (EEs)
- Both components affect all kits as well, including mod-added ones

v4.2
- Cleaned up the setup.tra file (the text that appears in the weidu installer). The file's actually readable now.
- Classic BG2: fixed small bug with nymph scripts, relating to using Cause Serious Wounds spell.
- a few other small edits to various installer files

v4.1
- Removed the following components:
	- Fix weapon styles for some kits, if incorrectly changed by a tweak (EEs)
	- Weapon Style tweak for Deities of Faerun (EEs)
- I still use these, but I decided they didn't fit in this mod. I have an informal mod that still has these components. It can be downloaded from this post in the Beamdog forums: https://forums.beamdog.com/discussion/comment/1182256/#Comment_1182256

v4.0
- Moved backup folder to weidu_external (instead of mod folder).
- Added HANDLE_CHARSETS function for installing on non-EE games.
- Adjust enemy damage at higher difficulties (classic IWD, IWD2):
	- now compatible with IWD2 (take normal damage on Insane/HoF, instead of double damage)
	- requires patching iwd2.exe (code by Bubb, used with permission)

v3.9
- Auto-assign script works smoother. It will only trigger now if the character is idle. In previous versions, it was interrupting movement if the player moved before the script was set. This only happened once or twice per character, but it should no longer happen.

v3.8
- classic BG2 (script)
	- TobEx Afterlife was updated since the v3.7. I changed it so that the DLL packaged with this mod will not be added if TobEx Afterlife is detected. This also means that starting from this version, you must be using the latest version of TobEx Afterlife (v29.10 or later). Older versions are missing the DLL fixes.
	- Improved GUI mod was also updated. I did some testing and didn't notice any issues, but just in case, I added a check for a few components to skip copying the DLL. Use v5.1 or later.

v3.7
- classic BG2 (script):
	- added fixed DLL file if TobEx is detected (made by Insomniator from Spellhold Studios forum)
	- fixed compatibility issue with Extended Event Text component from Improved GUI mod
- Better AI for Call Woodland Beings
	- now compatible with original BG2 engine
	- as with the EEs, the patch option is compatible with atweaks PnP Fey
- "Give party starting equipment" tweak:
	- IWD-in-BG2: fixed potential issues caused by AR1006.BCS (starting area script)
	- classic IWD1: fixed items sometimes not being added if using an existing save

v3.6
- Call Woodland Beings - patch option (EEs)
	- atweaks summons will correctly have the item RR#DINV.ITM destroyed automatically when summoned
	- was being prevented because my patch prevents AI actions while invisible (the item makes them invisible)

v3.5
- Call Woodland Beings AI (EEs)
	- added subcomponent: Use existing script, but patch in a few actions
	- adds Cooldown hotkeys (B to enable, E to disable)
	- adds D hotkey to teleport to party
	- will teleport to party if not in visual range (and not invisible)
	- will preserve invisibility
	- usable with atweaks PNP Fey, as well as AI mods that still use NYMPH.BCS (ex. SCS)
- Give party starting equipment (IWD games)
	- Option 1 (auto-equip) is now skipped if certain tweaks are installed
	- Option 2 (start with items in a bag) can be used with any tweaks
	- detects BG/IWD-style profs (from cdtweaks) and Proficiency Overhaul (from Skill and Abilities mod)
- classic BG2
	- the party script will fail to install if the Extended Event Text component from Improved GUI mod is detected (also called Extended messages/sounds or Extended Items/Quest/Spell messages)
	- installing these together will crash the game when attempting to load a save
- fixed/added info in readme, relating to the experimental gold-exchanging Bag of Holding option (EEs)


v3.4
- minor adjustments to party scripts
- added tweak: Patch visuals for shortbows (IWD:EE) and scimitars (IWD-in-BG2)
- IWD2: minor update to "starting equipment" - bag option

v3.3.1
- for "Give party starting equipment" - bag option:
	- IWD2: minor fix + added a greatsword to the bag
	- IWDEE: added a scimitar to the bag (the ninjato is still there)

v3.3
Small upate to scripts:
- the B and E hotkeys (Cooldown Mode) now give feedback in the dialogue box

Call Woodland Beings script
- will now be skipped if the atweaks PNP Fey component is installed. It's not impossible to make it compatible, but I don't have time for that right now.

Changes/fixes for the "Give party starting equipment" tweak:
- IWD-in-BG2: greataxe was set to wrong item resource
- classic IWD1 (with component 1):
	- improved scripting
	- more ranged weapons can spawn
	
- Added a new subcomponent:
	- Component 1: This is the original component. It auto-equips or adds weapons to inventory. The way items are chosen is game-dependent. For IWDEE, it's based on proficiencies, and currently only supports the unmodded prof system.
	- Component 2: Instead of adding to inventory, this component will give the party a bag, containing a selection of weapons. A single bag is given and the player can choose what to do with unwanted items (i.e. sell or throw away).
	
NOTE: If the separate "Give party a Bag of Holding" component is not installed, then items can only be taken out of the weapon bag. If it is installed, then the bag is changed to a normal Bag of Holding. You only have one bag with both installed, and install order doesn't matter.

v3.2
- Added component: Auto-assign script to new characters. This is a one-time action for each character in the party. Joinable NPCs in the EEs will also have their starting script changed.

- Added the following tweaks:
	- Misc fixes for backstab-related 2DA files (EEs)
	- Reduce delay for Sneak Attacks + uncap Crippling Strike (EEs)
	- Fix weapon styles for some kits, if incorrectly changed by a tweak (EEs)
	- Weapon Style tweak for Deities of Faerun (EEs)
	- Allow Minsc to use his Berserk ability at will (BG games)

v3.1
- minor update, but I want to make sure the info's accurate
- updated readme info for the experimental Bag of Holding option; key things to note:
	- Charisma of the active character adjusts the price for buying items back (in the v3.0, I mistakenly wrote that it used the party leader's Charisma)
	- items with 1 gold base price will always give 0 gold when putting in the bag; there's no way to change this (that I know of), even setting it to 100+% will still give 0 gold
	- items with 0 gold base price are free to transfer either way (ex. regular arrows)
- I also lowered the markup for taking items out of the bag (it was stupidly high); this makes it easier to use the exploit, but people who want to use it will use it regardless, since there's no way to completely remove it

v3.0
- Fixed an issue where some Bioware NPCs could target each other for 1-2 seconds after killing enemies. I didn't notice this until recently because I did most of my early testing with custom characters only.

- Removed Calls for Help responses. I think what I had was pretty good, but it took away control from the player, which goes against the intent of a minimalist script. Shout actions are still in the script, in case I want to use them later (they should have a negligible effect on efficiency).

- Added support for classic Baldur's Gate (that's BG1 on the BG1 engine). Key info:
	- characters will preserve Hide/Invisibility/Sanctuary
	- melee aggro ranges working
	- calls for help working (REMOVED, but theoretically, I could add it back in)
	- Cooldown hotkeys working
	- no auto-Search (the FindTraps() script action doesn't work)
	- Bard Song, Turn Undead, and Search won't prevent auto-attacking, but you can keep them active during battle if the character is standing outside melee aggro range (obviously with a melee weapon equipped)

- Added the following tweaks:
	- EEs: Allow movement bonuses from shapeshift forms to bypass Free Action
	- IWDEE: Increase movement speed of Winter Wolf and Polar Bear forms
	- Give party starting equipment (IWD games)
	- Give party a Bag of Holding at game start (classic and EEs)
	- All classes get full HP bonuses from Constitution (classic and EEs)

- Tested and confirmed that the BG2 script is working with various conversion mods, including IWD-in-BG2, Classic Adventures, and Epic Endeavors. The Bag of Holding tweak is also working with these.

- This mod is pretty much finished now besides bug fixes, or making minor adjustments. The only TODO I have planned in my notes is PsT:EE support, which I'll probably only add if/when I get around to replaying it.


v2.5
- added Beta support for original BG2/Tutu/BGT and IWD1; a few incompatible triggers or blocks had to be removed for each game (the core features of the script are in); I'm calling this a Beta because I only did very limited testing + made sure they look okay in NearInfinity
- added a few tweak options for IWD1 and IWD2

v2.4
- fixed regression, caused by dumb ordering of blocks, that prevented Bard Song from stopping when invisible
- IWD2: I noticed unexpected (and undocumented on IESDP) behavior from the Attack() action; I've changed one of the Attack() actions to AttackOneRound() because it could lock a character into auto-attacking (ignoring the triggers in the script)

v2.3
- fixed an additional error in the IWD2 script; this is just rearranging some OR() groups (which I just learned work slightly differently from the other games)

v2.2
- fixed some triggers that I realized were scripted wrong; gameplay effect is minimal

v2.1
- fixed nymph summon not detecting invisible PCs, causing it to use Dimension Door repeatedly (it's scripted to teleport to the party if out of range)
- nymph summon will no longer use Dimension Door if invisible (because it removes the invisibility); the D hotkey can still be used to force teleport it

v2.0
- rework of auto-attack, main thing is improved retargeting scripting
- added Cooldown hotkeys (B to enter for 5 rounds, E to deactivate); reduces melee aggro range to 5 ft.
- IWDEE: in Dragon's Eye 5th floor, will not attack certain targets that reduce reputation if killed
- IWD2: when responding to a call for help, ranged attackers will no longer follow into melee range (will stop 15 ft. or further away)
- EEs: added calls for help (Shout action/response), using similar scripting as IWD2
- EEs: added an improved AI script for the nymph summon (Call Woodland Beings)

v1.3
- small update, should reduce delay for auto-attack at start of combat

v1.2
- another rework of the scripting for enemies with weapon/damage immunity; it combines stuff from v1.0 and v1.1, but it's mostly based on the v1.0
- increased likelihood of character stopping attacking, if suddenly invisible (for example, from a contingency or area invisibility spell); not 100% reliable (can't stop an attack already initiated) and only works when fighting actual enemies

v1.1
- renamed BAF files (script file is still iwdpgen.BS)
- Rewrote the scripting for facing enemies with weapon/damage immunity

v1.0
- Changes to auto-attack conditions for some classes (see breakdown for updated info)
- Improved scripting when facing enemies with weapon/damage immunity
- Improved auto-run behavior (when holding a ranged weapon in melee range); it no longer overrides user commands, but is still checked once per round if auto-attacking

v0.9
- added some limited prioritizing of enemy casters (wizard, sorceror, cleric, druid, or bard); will attack these classes first, but only if within range of the currently equipped weapon, or under 5 ft. away (can still target other enemies sometimes)
- subtle improvements to auto-attack or auto-Search in specific situations
- edits to various blocks in the script file, either fixing incorrect behavior or to remove redundant triggers

v0.8
- EEs: better targeting of enemies with weapon immunity (it's not 100%, may still target immune enemies, but makes it more likely to attack enemies you can actually hit)
- all games: if a character becomes invisible while playing a Bard Song, the song will stop to preserve invisibility (Shamanic Dance will not stop to preserve summons)
- all games: if using a ranged weapon, will back away if a melee attacker gets too close (only a small amount, it's mainly to give visual feedback in case the player wasn't paying attention)
- all games: at near-death, won't auto-attack unless target is in range of current weapon (this allows you to pull a character away from a scrum, and not worry about them rushing back in before being healed)

v0.7
- Melee auto-attacking conditions added for all classes (set to my own personal preferences)
- Overall improvements to auto-attack and auto-search behavior

v0.6
- fixed auto-Search activating during Stealth (for IWD2, I'd recommend putting Stealth directly on the quick bar, instead of using it from the Skills menu)

v0.4
- added additional restrictions to auto-attacking for mages and sorcerers (see auto-attack details)

v0.3
- added auto-Search during combat, if invisible or sanctuaried; will not auto-Search if character is using Turn Undead or Shamanic Dance (EEs), or using Battle Song (IWD2), because these abilities don't break the Sanctuary effect

v0.2
- usable with IWD2, BGEE, BG2EE and EET
- added Shaman detect illusion to script

v0.1
- adds Shamanic Dance to list of abilities that prevent auto-attack
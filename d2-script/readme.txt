Better IWD Pregen (v5.0)
GitHub: https://github.com/D2-mods/Better-IWD-Pregen
Compatibility: Classic and EE versions of BG1, BG2, IWD, and IWD2


==================================================
OVERVIEW
==================================================
A minimalist script and tweak pack. This mod was started as an attempt to make an improved version of the IWD Pregen script from IWD:EE. Compatible with classic and EE versions of BG1, BG2, IWD, and IWD2.


==================================================
INSTALL
==================================================
Extract to game folder and run the setup to install or uninstall. I'm not familiar with Mac/Linux, but installing should be the same as other mods (mod packages are cross-platform). It's best to install this mod near the end of the order.

Script components:
1. Better IWD Pregen (appears in-game as "IWD PREGEN")
2. Better AI for Call Woodland Beings (EEs, BG2), install after AI mods (ex. SCS or atweaks)
3. Auto-assign script to new characters

Tweak components:
1. Adjust enemy damage at higher difficulties (classic IWD, IWD2)
2. Add or remove Avarine Decanter (IWD2)
3. Unnerf Animate Dead (IWD2)
4. Shapeshift movement bonuses bypass Free Action (EEs)
5. Increase movement speed of Winter Wolf and Polar Bear forms (IWD:EE)
6. Give party starting equipment (IWD games)
7. Give party a Bag of Holding at game start (classic and EEs)
8. All classes get full HP bonuses from Constitution (classic and EEs)
9. Fixes for backstab-related 2DA files (EEs)
10. Reduce delay for Sneak Attacks + uncap Crippling Strike (EEs)
11. Allow Minsc to use his Berserk ability at will (BG games)
12. Patch visuals for shortbows (IWD:EE) or scimitars (IWD-in-BG2)
13. Remove alignment restrictions for classes (classic and EEs)
14. Paladins and Rangers do not fall at low rep (EEs)

Additional info:
- All components can be installed independently and in any order, except for auto-assigning the script.
- Any similar components in this mod and my other mods should have no conflicts if installed together.
- All tweak components have at least 2 subcomponents (even if just a simple "Yes" or "No")


==================================================
SCRIPT COMPATIBILITY (v4.0)
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
IN-GAME DESCRIPTION (adjusted for each game)
==================================================
IWD PREGEN: The character will auto-attack when enemies are in range*, but will not attack if under the effects of Invisibility or Sanctuary, or if using Stealth, Bard Song, Turn Undead, or Shamanic Dance. If not in auto-attack range, a Thief, Monk, or Shaman will search for traps or illusions, but not if using Stealth, Turn Undead, or Shamanic Dance. (<script>)

*Melee auto-attack range is dependent on class (see readme for full breakdown).

Cooldown mode: Reduces melee aggro range to 5 feet. Press the B key to enter for 5 rounds, or the E key to deactivate instantly.


==================================================
CREDITS
==================================================
Modder: Dan_P

Custom Functions:
- CD_EXTEND-O-MATIC, by CamDawg (https://www.gibberlings3.net/forums/topic/28835-toss-your-semi-useful-weidu-macros-here/#comment-254220)
- 2DA_MISSING_COLS - by K4thos (https://github.com/K4thos/IE-code-repository)
- The other files include simple functions I put together to do stuff.

Tools and Resources used:
- WeiDU (https://github.com/WeiDUorg/weidu)
- NearInfinity (https://github.com/Argent77/NearInfinity)
- Notepad++ (https://notepad-plus-plus.org/)
- Git Bash (https://git-scm.com/downloads)
- Infinity Auto Packager (https://github.com/InfinityTools/InfinityAutoPackager)
- IESDP (https://gibberlings3.github.io/iesdp/main.htm)
- LibIconv for Windows (http://gnuwin32.sourceforge.net/packages/libiconv.htm)

TobEx.dll:
- Patched DLL file was made by Insomniator and used with permission.
- http://www.shsforums.net/topic/61135-question-about-featurebug-change-to-the-noaction-script-action/#entry612382

IWD2 exe patch:
- Patch for the enemy damage component was written by Bubb and used with permission.
- https://www.gibberlings3.net/forums/topic/35670-adjusting-difficulty-levels-iwd2/#comment-311240


==================================================
VERSION INFO
==================================================
v5.1
- EEs: Any character with skill points in detecting traps or illusions will not have auto-Search enabled. Previously, the feature was only for specific classes.
- Cleaned up a few possible harmless warning messages.
- Some minor adjustments (not to scripts)

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
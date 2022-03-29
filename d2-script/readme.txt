Better IWD Pregen (v3.0+)
GitHub: https://github.com/D2-mods/Better-IWD-Pregen
Installs on: BG(EE), BG2(EE), IWD(EE), IWD2, EET, Tutu/BGT, and any mods built on these engines


==================================================
OVERVIEW
==================================================
The IWD Pregen script from IWD:EE basically does what I want an AI script to do, which is auto-attack, but not when invisible/hiding or using certain class abilities, like Bard Song or Turn Undead. It's a minimalist script that reduces some of the more frustrating aspects of auto-attacking.

What this mod does is take IWD Pregen, and finetune the auto-attack and auto-Search scripting (based on my own preferences), while keeping it minimalist. Spells, abilities, item use, etc., are for the player to micromanage.

The biggest difference you'll notice from the vanilla IWD Pregen is that non-warrior classes won't rush into melee combat unless they get closer to the enemy (range depending on class). This gives the player more control over the battle and more options for placement of characters, without needing to turn AI off.

UPDATE v2.0:
- rework of auto-attack, main thing is improved retargeting scripting
- added Cooldown hotkeys (B to enter for 5 rounds, E to deactivate); reduces melee aggro range to 5 ft.
- EEs: added an improved AI script for the nymph summon (Call Woodland Beings)


==================================================
INSTALL
==================================================
Extract to game folder and run the setup to install or uninstall. I'm not familiar with Mac/Linux, but installing should be the same as other mods (mod packages are cross-platform). It's best to install this mod near the end of the order.

Script components:
1. Better IWD Pregen (appears in-game as "IWD PREGEN")
2. EEs: Better AI for Call Woodland Beings (should be installed after SCS)
3. Auto-assign script to new characters

Tweak components:
1. Adjust enemy damage at higher difficulties (IWD1)
2. Add or remove Avarine Decanter (IWD2)
3. Unnerf Animate Dead (IWD2)
4. Allow movement bonuses from shapeshift forms to bypass Free Action (EEs)
5. Increase movement speed of Winter Wolf and Polar Bear forms (IWD:EE)
6. Give party starting equipment (IWD games)
7. Give party a Bag of Holding at game start (classic and EEs)
8. All classes get full HP bonuses from Constitution (classic and EEs)
9. Misc fixes for backstab-related 2DA files (EEs)
10. Reduce delay for Sneak Attacks + uncap Crippling Strike (EEs)
11. Fix weapon styles for some kits, if incorrectly changed by a tweak (EEs)
12. Weapon Style tweak for Deities of Faerun (EEs)
13. Allow Minsc to use his Berserk ability at will (BG games)
14. Patch visuals for shortbows (IWD:EE) and scimitars (IWD-in-BG2)

All components can be installed independently and in any order, except for auto-assigning the script.


==================================================
COMPATIBILITY (v3.0+)
==================================================
EEs: BG:EE, SoD, BG2:EE, IWD:EE, EET (v2.5/v2.6)
Classic: BG1, BG2, IWD1, IWD2 (tested with GOG versions)

TobEx (v26/v28): If TobEx is installed, the BG2 script will deactivate the Expanded Actions hack (because it breaks the script for some classes). The issue is caused by Expanded Actions changing the behavior of the NoAction() script action to disable Modal states (ex. Bard Song). Note that the normal behavior in all IE games, from classic BG1 to the EEs, is that NoAction() does not disable Modal states. If TobEx files are added as a part of other mods, Expanded Actions will not be deactivated, unless issues are observed/reported with a specific mod.

IWD-in-BG2: Tested and working.
Tutu/BGT: Untested but installable.
Classic Adventures: Tested and working.
Epic Endeavors: Tested and working.

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
Coding, Testing: Dan_P

Custom Functions:
- CD_EXTEND-O-MATIC, by CamDawg (https://www.gibberlings3.net/forums/topic/28835-toss-your-semi-useful-weidu-macros-here/#comment-254220)
- 2DA_MISSING_COLS - by K4thos (https://github.com/K4thos/IE-code-repository)

Tools and Resources used:  
- WeiDU v249 https://github.com/WeiDUorg/weidu  
- NearInfinity v2.2-20211218 https://github.com/Argent77/NearInfinity  
- Notepad++ https://notepad-plus-plus.org/  
- Git Bash https://git-scm.com/downloads  
- Infinity Auto Packager https://github.com/InfinityTools/InfinityAutoPackager  
- IESDP https://gibberlings3.github.io/iesdp/index.htm


==================================================
VERSION INFO
==================================================
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
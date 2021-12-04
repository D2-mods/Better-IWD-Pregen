Better IWD Pregen - a minimalist script for all classes
GitHub: https://github.com/D2-mods/Better-IWD-Pregen
Game version: BG:EE, BG2:EE, IWD:EE, IWD2, EET


==================================================
OVERVIEW
==================================================
The IWD Pregen script from IWD:EE basically does what I want an AI script to do, which is auto-attack, but not when invisible/hiding or using certain class abilities, like Bard Song or Turn Undead. It's a minimalist script that reduces some of the more frustrating aspects of auto-attacking.

What this mod does is take IWD Pregen, and finetune the auto-attack and auto-Search scripting (based on my own preferences), while keeping it minimalist. Spells, abilities, item use, etc., are for the player to micromanage.

The biggest difference you'll notice from the vanilla IWD Pregen is that non-warrior classes won't rush into melee combat unless they get closer to the enemy (range depending on class). This gives the player more control over the battle, and more options for placement of characters, without needing to turn AI off.

UPDATE v2.0:
- rework of auto-attack, main thing is improved retargeting scripting
- added Cooldown hotkeys (B to enter for 5 rounds, E to deactivate); reduces melee aggro range to 5 ft.
- EEs: added an improved AI script for the nymph summon (Call Woodland Beings)


==================================================
INSTALL
==================================================
Extract to game folder and run the setup to install or uninstall. I'm not familiar with Mac/Linux, but installing should be the same as other mods (mod packages are cross-platform). It's best to install this mod near the end of the order. It shouldn't affect other mods, unless they also use the files iwdpgen.BS or NYMPH.BCS.

This mod has 2 components:
1. Better IWD Pregen (appears in-game as "IWD PREGEN")
2. EEs only: Better AI for Call Woodland Beings (should be installed after SCS)


==================================================
DESCRIPTIONS
==================================================
EEs
IWD PREGEN: The character will auto-attack when enemies are in range, but will not attack if under the effects of Invisibility or Sanctuary, or if using Stealth, Bard Song, Turn Undead, or Shamanic Dance. If not in auto-attack range, a Thief, Monk, or Shaman will search for traps or illusions, but not if using Stealth, Turn Undead, or Shamanic Dance.

IWD2
IWD PREGEN: The character will auto-attack when enemies are in range, but will not attack if under the effects of Invisibility or Sanctuary, or if using Stealth or Battle Song. If not in auto-attack range, a character with Rogue or Monk levels** will search for traps, but not if using Stealth or Battle Song.

**for auto-Search, only characters with Rogue or Monk levels will automatically use the Search ability, even if you remove the class restrictions from the script. This seems to be hardcoded or hidden in a file somewhere.


==================================================
Auto-attack breakdown:
==================================================
EEs
Class: Fighter, Ranger, Paladin, including any multiclass combinations
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 25 ft.
	3. Attacked by enemy
	4. If not in sight of enemies, can respond to a call for help

Class: Kensai, Monk, Shapeshift/Polymorph (without Fighter levels)
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 18 ft.
	3. Attacked by enemy
	4. If not in sight of enemies, can respond to a call for help

Class: Cleric, Druid, Shaman, Thief, Bard, Cleric/Thief
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 12 ft.

Class: Mage, Sorcerer, Mage/Thief, Cleric/Mage
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 3 ft.
	3. If THAC0 is less than 5, will attack if enemy is within 12 ft.

IWD2
Class: Fighter, Ranger, Paladin or Barbarian (single-class or multiclass with 3+ levels)
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 25 ft.
	3. Attacked by enemy
	4. Level 3+: If not in sight of enemies, can respond to a call for help

Class: Monk (Level 9+), Wild Shape/Tenser's/Iron Body (without 3+ warrior levels)
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 18 ft.
	3. Attacked by enemy
	4. If not in sight of enemies, can respond to a call for help

Class: Cleric, Druid, Monk, Thief or Bard, including multiclass with Wizard or Sorcerer
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 12 ft.

Class: Wizard or Sorcerer
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 3 ft.


==================================================
Calls for help info (Shout action/response):
==================================================
A Shout action is made when initially seeing an enemy, immediately after responding to a Shout, or repeatedly if idling in battle (i.e. standing outside melee range).

Response: If not in sight of enemies, the character can respond to a Shout, moving towards the caller. This action continues until either the character reaches the caller, or an enemy is within 15 feet.

Characters will not use or respond to a Shout if under the effects of Invisibility or Sanctuary, or if using Stealth, Bard Song, Turn Undead, or Shamanic Dance. A character in Cooldown mode can make a Shout, but will not respond to one.


==================================================
Better AI for Call Woodland Beings
==================================================
Info:
- not as wasteful with spells
- won't cast statuses on undead or enemies with high magic resist
- will teleport to catch up with the party (i.e. while traveling with Boots of Speed)
- is more cautious at low HP if it has spells remaining
- will not attack or cast spells at enemies if invisible
- Cooldown hotkeys to delay spellcasting

Compatible with BG:EE, BG2:EE, IWD:EE and EET.

DDoor: As in the unmodded script, the nymph may use Dimension Door at will if conditions are met. It will alway teleport to either the nearest enemy or to a PC (usually, its summoner).

Marking: The nymph "marks" a PC as an object for various actions (by default, this is the summoner). If the marked PC is not on the map for any reason, the nymph will choose another PC on the same map. The nymph will always switch back to its summoner if in visual range. Note that the summoner, as an identifier, is not saved if a summon is still on the map (so if reloading, the script will default to Player1 as the "marked" PC).

Hotkeys:
- if the D key is pressed outside of combat, and not in visual range of enemies, the nymph will teleport to its summoner (or other PC)
- if the B key is pressed, the nymph will enter Cooldown for 3 rounds; will not cast offensive spells or teleport to an enemy in Cooldown mode
- if the E key is pressed, the Cooldown timer is set to 0 (deactivated)


==================================================
CREDITS
==================================================
Coding, Testing: Dan_P

Tools and Resources used:  
- WeiDU v249 https://github.com/WeiDUorg/weidu  
- NearInfinity v2.2-20210501 https://github.com/Argent77/NearInfinity  
- Notepad++ https://notepad-plus-plus.org/  
- Git Bash https://git-scm.com/downloads  
- Infinity Auto Packager https://github.com/InfinityTools/InfinityAutoPackager  
- IESDP https://gibberlings3.github.io/iesdp/index.htm


==================================================
VERSION INFO
==================================================
v2.4
- fixed regression, caused by dumb ordering of blocks, that prevented Bard Song from stopping when invisible
- IWD2: I noticed unexpected (and undocumented on IESDP) behavior from the Attack() action in IWD2; I've changed one of the Attack() actions to AttackOneRound() because it could lock a character into auto-attacking (ignoring the triggers in the script)

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
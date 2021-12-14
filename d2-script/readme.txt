Better IWD Pregen - a minimalist script for all classes
GitHub: https://github.com/D2-mods/Better-IWD-Pregen
Installs on: BG:EE, BG2:EE, IWD:EE, IWD2, EET, BG2/Tutu/BGT (Beta), IWD1 (Beta)


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
Extract to game folder and run the setup to install or uninstall. I'm not familiar with Mac/Linux, but installing should be the same as other mods (mod packages are cross-platform). It's best to install this mod near the end of the order. The scripts shouldn't affect other mods, unless they also use the files iwdpgen.BS or NYMPH.BCS.

Script components:
1. Better IWD Pregen (appears in-game as "IWD PREGEN")
2. EEs only: Better AI for Call Woodland Beings (should be installed after SCS)

Tweak components:
1. Adjust enemy damage at higher difficulties (IWD1)
2. Add or remove Avarine Decanter (IWD2)
3. Unnerf Animate Dead (IWD2)


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
- CD_EXTEND-O-MATIC, from CamDawg, posted at <https://www.gibberlings3.net/forums/topic/28835-toss-your-semi-useful-weidu-macros-here/#comment-254220>

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
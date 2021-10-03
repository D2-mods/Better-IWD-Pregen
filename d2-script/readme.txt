Updated IWD Pregen script (for EEs and IWD2)
Game version: IWD:EE, IWD2, BG:EE, BG2:EE, EET


OVERVIEW:

The IWD Pregen script from IWD:EE basically does what I want an AI script to do, which is auto-attack, but not when invisible/hidden or using certain class abilities. It does not switch targets without your input, and does not switch weapons, unless a ranged weapon runs out of ammo. I like to micro-manage everything else.

I originally made this mod for IWD:EE to add Shamanic Dance to the list of abilities that prevent auto-attack, because Beamdog hasn't added it in, as of v2.6. I then decided to make a similar script for IWD2, because none of the base game scripts are similar. You can also use this with BG:EE, BG2:EE and EET.

Note: some classes have additional restrictions for auto-attacking (see below)


INSTALLATION:

Extract to game folder and run the setup to install or uninstall. I'm not familiar with Mac/Linux, but installing should be the same as other mods (mod packages are cross-platform).


DESCRIPTIONS:

EEs
IWD PREGEN: The character will auto-attack when enemies are sighted, but will not attack if under the effects of Invisibility or Sanctuary, or if using Stealth, Bard Song, Turn Undead, or Shamanic Dance. If no enemies are nearby, a Thief, Monk, or Shaman will search for traps or illusions, but not if using Stealth, Turn Undead, or Shamanic Dance.

IWD2
IWD PREGEN: The character will auto-attack when enemies are sighted, but will not attack if under the effects of Invisibility or Sanctuary, or if using Stealth or Battle Song. If no enemies are nearby, a character with Rogue or Monk levels will search for traps, but not if using Stealth or Battle Song.


Additional info:

EEs
- single-class mages and sorcerers will only auto-attack if one of the following conditions is met:
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 3 ft.
	3. Polymorphed
	4. THAC0 is less than 5

IWD2
- characters with wizard or sorcerer levels will only auto-attack if one of the following conditions is met:
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 3 ft.
	3. Tenser's Transformation is in effect
	4. Druid Shapeshift
	5. Level 3+ in Fighter, Ranger, Paladin, Monk, or Barbarian
- for auto-Search, I didn't actually put class restrictions in the script. However, from my testing, only characters with rogue or monk levels will automatically use the Search ability.


CREDITS:

Coding, Testing: Dan_P

Resources:
IESDP
NearInfinity
WeiDU readme


VERSION INFO:

v0.4
- added additional restrictions to auto-attacking for mages and sorcerers

v0.3
- added auto-search during combat, if invisible or sanctuaried; will not auto-search if character is using Turn Undead or Shamanic Dance (EEs), or using Battle Song (IWD2), because these abilities don't break the Sanctuary effect

v0.2
- usable with IWD2, BGEE, BG2EE and EET
- added Shaman detect illusion to script
- reorganized folder structure

v0.1
- initial release
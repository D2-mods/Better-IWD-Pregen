==================================================
Script - Quick Info
==================================================
- Better IWD Pregen (d2scrp): Base script. Includes all features listed below.
- d2scrp-: Same as base script, except default mode is Cooldown.
- d2scrp+: Same as base script, except calls for help are enabled.
- IWD Pregen (iwdpgen): Same as vanilla IWD Pregen, but with shaman abilities added. (EE-only)


==================================================
Auto-attack features
==================================================
- Melee aggro range is dependent on class (see below for full breakdown).
- Will not attack if under the effects of Invisibility or Sanctuary.
- Will not attack if using Stealth, Bard Song, Turn Undead or Shamanic Dance.
- EEs: Active retargeting if a character's current weapon cannot hit or damage an enemy.
- Priority targeting against enemy casters (limited to within 5 ft. or in range of current weapon).
- Cooldown hotkeys to reduce melee aggro range to 5 ft. for 30 seconds, or set back to normal instantly.


==================================================
Other features
==================================================
- Classes with Search will use it when not attacking (note: for IWD2, auto-Search only works if a character has Rogue or Monk levels).
- Will not auto-Search if using Stealth, Bard Song, Turn Undead or Shamanic Dance.
- Will attempt to stop attacking, or stop a Bard Song, if suddenly invisible (ex. from a contingency or area invisibility spell).
- Shamanic Dance is NOT stopped if suddenly invisible. This is to preserve summons.
- Will not auto-attack at under 15% HP, unless an enemy is in range of current weapon.


==================================================
Cooldown hotkeys
==================================================
- If the B key is pressed, the character will enter a Cooldown mode for 30 seconds.
	- Reduces melee aggro range to 5 ft..
	- Also disables some of the retargeting actions.
- If the E key is pressed, the Cooldown mode will be deactivated.
- If the game is saved while a character is in Cooldown mode, it will be deactivated on reload.

Note: Stealth, Bard Song, Turn Undead and Shamanic Dance will prevent any Cooldown-related actions from triggering.


==================================================
Auto-assign script (separate component)
==================================================
- Gives new party members the Better IWD Pregen script.
- Will trigger once for each character per game.
- NPC characters should have AI changed before casting any spells.

Note: For BG1, this will trigger once per party slot per playthrough (Player1, Player2, etc.).



Additional info:

==================================================
Auto-attack breakdown (BG(EE), BG2(EE), IWD(EE))
==================================================
Class: Fighter, Ranger, Paladin, including any multiclass combinations
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 25 ft.
	3. Attacked by enemy

Class: Kensai, Monk, Shapeshift/Polymorph (without Fighter levels)
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 18 ft.
	3. Attacked by enemy

Class: Cleric, Druid, Shaman, Thief, Bard, Cleric/Thief
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 12 ft.

Class: Mage, Sorcerer, Mage/Thief, Cleric/Mage
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 3 ft.
	3. If THAC0 is less than 5, will attack if enemy is within 12 ft.


==================================================
Auto-attack breakdown (IWD2)
==================================================
Class: Fighter, Ranger, Paladin or Barbarian (single-class or multiclass with 3+ levels)
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 25 ft.
	3. Attacked by enemy

Class: Monk (Level 9+), Wild Shape/Tenser's/Iron Body (without 3+ warrior levels)
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 18 ft.
	3. Attacked by enemy

Class: Cleric, Druid, Monk, Thief or Bard, including multiclass with Wizard or Sorcerer
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 12 ft.

Class: Wizard or Sorcerer
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 3 ft.


==================================================
Baldur's Gate (in BG1 engine) - script info
==================================================
- Characters will preserve Hide/Invisibility/Sanctuary
- Melee aggro ranges working
- Calls for help working (d2scrp+)
- Cooldown hotkeys working
- No auto-Search (the FindTraps() script action doesn't work)

Note: Bard Song and Turn Undead won't prevent auto-attacking, but you can keep them active during battle if the character is standing outside melee aggro range (obviously with a melee weapon equipped).


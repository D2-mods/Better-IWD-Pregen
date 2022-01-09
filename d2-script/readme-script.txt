==================================================
Auto-attack features
==================================================
- melee aggro range is dependent on class; range from 3 ft. (mages) to 25 ft.
- will not attack if under the effects of Invisibility or Sanctuary
- will not attack if using Stealth, Bard Song, Turn Undead or Shamanic Dance
- EEs: active retargeting if a character's current weapon cannot hit or damage an enemy
- priority targeting against enemy casters (limited to within 5 ft. or in range of current weapon)
- Cooldown hotkeys to reduce melee aggro range to 5 ft. for 5 rounds, or set back to normal instantly


==================================================
Other features
==================================================
- classes with Search will use it whenever not attacking (note: IWD2 is hardcoded for only Rogues and Monks to be able to auto-Search)
- will not auto-Search if using Stealth, Bard Song, Turn Undead or Shamanic Dance
- will attempt to stop attacking, or stop a Bard Song, if suddenly invisible (for example, from a contingency or area invisibility spell)
- will not auto-attack at under 15% HP, unless an enemy is in range of current weapon
- ***REMOVED*** Calls for help (Shout action/response)


==================================================
Cooldown hotkeys
==================================================
- if the B key is pressed, the character will enter a Cooldown mode for 5 rounds, during which melee aggro range is reduced to 5 ft.; also deactivates some (but not all) of the retargeting actions; this mode can be set again at any time, even while active
- if the E key is pressed, the Cooldown mode will be deactivated
- both these keys can also be used as "stop action" buttons, as they will override other actions
- if the game is saved while a character is in Cooldown mode, it will be deactivated on reload

Note: Stealth, Bard Song, Turn Undead and Shamanic Dance will prevent any Cooldown-related actions from triggering


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
- characters will preserve Hide/Invisibility/Sanctuary
- melee aggro ranges working
- Calls for help working (REMOVED, but theoretically, I could add it back in)
- Cooldown hotkeys working
- no auto-Search (the FindTraps() script action doesn't work)
- Bard Song, Turn Undead, and Search won't prevent auto-attacking, but you can keep them active during battle if the character is standing outside melee aggro range (obviously with a melee weapon equipped)


==================================================
Calls for help info (Shout action/response)
==================================================
NOTE: This feature was added in v2.0 and removed in the v3.0. It actually works pretty good, but I decided it's too active of an action for a minimalist script, even with being able to disable it with the Cooldown mode.


A Shout action is made when initially seeing an enemy, immediately after responding to a Shout, or repeatedly if idling in battle (i.e. standing outside melee range).

Response: If not in sight of enemies, the character can respond to a Shout, moving towards the caller. This action continues until either the character reaches the caller, or an enemy is within 15 feet.

Characters will not use or respond to a Shout if under the effects of Invisibility or Sanctuary, or if using Stealth, Bard Song, Turn Undead, or Shamanic Dance. A character in Cooldown mode can make a Shout, but will not respond to one.


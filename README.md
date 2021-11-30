# Better IWD Pregen
Download: https://github.com/D2-mods/Better-IWD-Pregen/releases  
Game version: BG:EE, BG2:EE, IWD:EE, IWD2, EET

#### Overview:
This script manages auto-attack, while giving more nuanced control of the characters, so the player can focus on tactics and usage of spells and abilities to win battles. The script will never use your consumable items, spells, or abilities. What it does is put you in position to better use these abilities, while reducing some of the more frustrating aspects of auto-attack.

Also, I'm normally not a fan of auto-using of abilities (for PCs), but Search is non-intrusive, and it's not unrealistic for characters trained in it to keep an eye on surroundings whenever possible, including during battle when not attacking.

#### Auto-attack features:
- melee aggro range is dependent on class (see readme for full breakdown); range from 3 ft. (mages) to 25 ft.
- will not attack if under the effects of Invisibility or Sanctuary
- will not attack if using Stealth, Bard Song, Turn Undead or Shamanic Dance
- EEs: active retargeting if a character's current weapon cannot hit or damage an enemy
- priority targeting against enemy casters (limited to within 5 ft. or in range of current weapon)
- Cooldown hotkeys to reduce melee aggro range to 5 ft. for 5 rounds, or set back to normal instantly

#### Other features:
- classes with Search will use it whenever not attacking (note: IWD2 is hardcoded for only Rogues and Monks to be able to auto-Search)
- will not auto-Search if using Stealth, Bard Song, Turn Undead or Shamanic Dance
- will attempt to stop attacking, or stop a Bard Song, if suddenly invisible (for example, from a contingency or area invisibility spell)
- will not auto-attack at under 15% HP, unless an enemy is in range of current weapon
- calls for help (Shout action/response); see readme for details

v2.0: added an improved AI script for the nymph summon (Call Woodland Beings)

#### Cooldown hotkeys:
- if the B key is pressed, the character will enter a Cooldown mode for 5 rounds, during which melee aggro range is reduced to 5 ft.; also deactivates some (but not all) of the retargeting actions; this mode can be set again at any time, even while active
- if the E key is pressed, the Cooldown mode will be deactivated
- both these keys can also be used as "stop action" buttons, as they will override other actions
- if the game is saved while a character is in Cooldown mode, it will be deactivated on reload

Note: Stealth, Bard Song, Turn Undead and Shamanic Dance will prevent any Cooldown-related actions from triggering

#### Additional info:
<details>
  <summary>A few notes on version differences</summary>
  
> v0.6: Similar to the vanilla IWD Pregen, except it accounts for Shaman abilities (Dance and Search); Mages and Sorcerers (single class only) have reduced melee aggro range

> v1.x: Uses the AttackOneRound() action to retarget every round, regardless of enemy; many of the core features of the script are implemented in some form

> v2.0+: Uses both Attack() and AttackReevaluate() + setting timers; retargeting only occurs if relevant enemies are in sight; characters will enter or exit an "autobattle" mode, depending on conditions, which will activate or deactivate parts of the script
  
</details>
<details>
  <summary>Auto-attack breakdown</summary>
  
#### EEs:
  ```
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
  ```

#### IWD2:
  ```
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
  ```
  
</details>
<details>
  <summary>Calls for help (Shout action/response)</summary>
  
> A Shout action is made when initially seeing an enemy, immediately after responding to a Shout, or repeatedly if idling in battle (i.e. standing outside melee range).

> Response: If not in sight of enemies, the character can respond to a Shout, moving towards the caller. This action continues until either the character reaches the caller, or an enemy is within 15 feet.

> Characters will not use or respond to a Shout if under the effects of Invisibility or Sanctuary, or if using Stealth, Bard Song, Turn Undead, or Shamanic Dance. A character in Cooldown mode can make a Shout, but will not respond to one.
  
</details>
<details>
  <summary>Nymph AI script (Call Woodland Beings)</summary>
  
  ```
Info:
- not as wasteful with spells
- won't cast statuses on undead or enemies with high magic resist
- will teleport to catch up with the party (i.e. while traveling with Boots of Speed)
- is more cautious at low HP if it has spells remaining
- will not attack or cast spells at enemies if invisible
- Cooldown hotkeys to delay spellcasting
  ```

Compatible with BG:EE, BG2:EE, IWD:EE and EET.

> DDoor: As in the unmodded script, the nymph may use Dimension Door at will if conditions are met. It will alway teleport to either the nearest enemy or to a PC (usually, its summoner).

> Marking: The nymph "marks" a PC as an object for various actions (by default, this is the summoner). If the marked PC is not on the map for any reason, the nymph will choose another PC on the same map. The nymph will always switch back to its summoner if in visual range. Note that the summoner, as an identifier, is not saved if a summon is still on the map (so if reloading, the script will default to Player1 as the "marked" PC).

Hotkeys:
- if the D key is pressed outside of combat, and not in visual range of enemies, the nymph will teleport to its summoner (or other PC)
- if the B key is pressed, the nymph will enter Cooldown for 3 rounds; will not cast offensive spells or teleport to an enemy in Cooldown mode
- if the E key is pressed, the Cooldown timer is set to 0 (deactivated)
  
</details>
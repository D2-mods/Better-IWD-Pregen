# Better IWD Pregen
Download: https://github.com/D2-mods/Better-IWD-Pregen/releases  
Installs on: BG(EE), BG2(EE), IWD(EE), IWD2, EET, Tutu/BGT, and any mods built on these engines

#### Components:
Script components:
  ```
1. Better IWD Pregen (appears in-game as "IWD PREGEN")
2. Better AI for Call Woodland Beings (EEs, BG2), install after AI mods (ex. SCS or atweaks)
3. Auto-assign script to new characters
  ```
Tweak components:
  ```
1. Adjust enemy damage at higher difficulties (classic IWD, IWD2)
2. Add or remove Avarine Decanter (IWD2)
3. Unnerf Animate Dead (IWD2)
4. Allow movement bonuses from shapeshift forms to bypass Free Action (EEs)
5. Increase movement speed of Winter Wolf and Polar Bear forms (IWD:EE)
6. Give party starting equipment (IWD games)
7. Give party a Bag of Holding at game start (classic and EEs)
8. All classes get full HP bonuses from Constitution (classic and EEs)
9. Misc fixes for backstab-related 2DA files (EEs)
10. Reduce delay for Sneak Attacks + uncap Crippling Strike (EEs)
11. Allow Minsc to use his Berserk ability at will (BG games)
12. Patch visuals for shortbows (IWD:EE) and scimitars (IWD-in-BG2)
  ```
All components can be installed independently and in any order, except for auto-assigning the script. Most of the options in the installer are pretty self-explanatory, but the mod folder also contains a readme detailing the tweaks, in case there's any confusion.

#### Overview (party script):
This script manages auto-attack, while giving more nuanced control of the characters, so the player can focus on tactics and usage of spells and abilities to win battles. The script will never use your consumable items, spells, or abilities. What it does is put you in position to better use these abilities, while reducing some of the more frustrating aspects of auto-attack.

#### Auto-attack features:
- melee aggro range is dependent on class (see readme for full breakdown); range from 3 ft. (mages) to 25 ft.
- will not attack if under the effects of Invisibility or Sanctuary
- will not attack if using Stealth, Bard Song, Turn Undead or Shamanic Dance
- EEs: active retargeting if a character's current weapon cannot hit or damage an enemy
- priority targeting against enemy casters (limited to within 5 ft. or in range of current weapon)
- Cooldown hotkeys to reduce melee aggro range to 5 ft. for 30 seconds, or set back to normal instantly

#### Other features:
- classes with Search will use it whenever not attacking (note: IWD2 is hardcoded for only Rogues and Monks to be able to auto-Search)
- will not auto-Search if using Stealth, Bard Song, Turn Undead or Shamanic Dance
- will attempt to stop attacking, or stop a Bard Song, if suddenly invisible (ex. from a contingency or area invisibility spell)
- will not auto-attack at under 15% HP, unless an enemy is in range of current weapon

#### Cooldown hotkeys:
- if the B key is pressed, the character will enter a Cooldown mode for 30 seconds, during which melee aggro range is reduced to 5 ft.; also deactivates some (but not all) of the retargeting actions; this mode can be set again at any time, even while active
- if the E key is pressed, the Cooldown mode will be deactivated
- if the game is saved while a character is in Cooldown mode, it will be deactivated on reload

Note: Stealth, Bard Song, Turn Undead and Shamanic Dance will prevent any Cooldown-related actions from triggering

#### Additional info:
<details>
  <summary>Script Compatibility</summary>
  
#### Info:
EEs: BG:EE, BG2:EE, IWD:EE, EET (tested on v2.5/v2.6)  
Classic: BG1, BG2, IWD, IWD2 (tested with GOG versions)

Also compatible with any BG2 conversion mods (ex. BGT or Classic Adventures).

Classic BG2 engine:  
TobEx (v26/v28): Compatibility issues should be fixed (v3.7 and later).  
TobEx Afterlife: Use v29.10 or later. (http://www.shsforums.net/files/file/1274-tobex-afterlife)  
Improved GUI mod: Use v5.1 or later. (http://www.shsforums.net/files/file/1265-bg2-improved-gui)

NOTE: I'm not 100% sure the scripts work with expansionless versions of the classic games.
  
</details>
<details>
  <summary>Auto-attack breakdown</summary>
  
#### BG(EE), BG2(EE), IWD(EE):
  ```
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
  ```

#### IWD2:
  ```
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
  ```
  
</details>
<details>
  <summary>Nymph AI script (Call Woodland Beings)</summary>
  
#### Option 1 - Revised script:
- smarter spellcasting (better targeting and not as wasteful)
- won't cast statuses on undead or enemies with high magic resist
- will teleport to catch up with the party (i.e. while traveling with Boots of Speed)
- is more cautious at low HP if it has spells remaining
- will not attack or cast spells at enemies if invisible
- Cooldown hotkeys to delay spellcasting

Compatible with EEs and original BG2 engine.  
Not compatible with atweaks PnP Fey (will be skipped during installation).

> DDoor: As in the unmodded script, the nymph may use Dimension Door at will if conditions are met. It will alway teleport to either the nearest enemy or to a PC (usually, its summoner). It will not use Dimension Door if invisible, unless instructed to by the player (with the D key).

> Marking: The nymph "marks" a PC as an object for various actions (by default, this is the summoner). If the marked PC is not on the map for any reason, the nymph will choose another PC on the same map. The nymph will always switch back to its summoner if in visual range. Note that the summoner, as an identifier, is not saved if a summon is still on the map (so if reloading, the script will default to Player1 as the "marked" PC).

Hotkeys:
- if the D key is pressed outside of combat, and not in visual range of enemies, the nymph will teleport to its summoner (or other PC)
- if the B key is pressed, the nymph will enter Cooldown for 3 rounds; will not cast offensive spells or teleport to an enemy in Cooldown mode
- if the E key is pressed, the Cooldown timer is set to 0 (deactivated)



#### Option 2 - Patch existing script:
- adds Cooldown hotkeys (B to enable, E to disable)
- adds D hotkey to teleport to party
- will teleport to party if not in visual range (and not invisible)
- will preserve invisibility
- usable with atweaks PnP Fey, as well as AI mods that still use NYMPH.BCS (ex. SCS)

NOTE: Dimension Door is more limited with this patch. Will only teleport to the summoner or Player1.
  
</details>
<details>
  <summary>Baldur's Gate (in BG1 engine)</summary>
  
#### BG1 script info:
- characters will preserve Hide/Invisibility/Sanctuary
- melee aggro ranges working
- Calls for help working (REMOVED, but theoretically, I could add it back in)
- Cooldown hotkeys working
- no auto-Search (the FindTraps() script action doesn't work)

NOTE: Bard Song and Turn Undead won't prevent auto-attacking, but you can keep them active during battle if the character is standing outside melee aggro range (obviously with a melee weapon equipped)
  
</details>
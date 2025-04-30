# Better IWD Pregen
Download: https://github.com/D2-mods/Better-IWD-Pregen/releases  
Supports: classic and EE versions of BG1, BG2, IWD, and IWD2 (including EET/BGT/IWD2EE).

--

A minimalist script and tweak pack for Infinity Engine games. This mod was started as an attempt to make an improved version of the "IWD Pregen" party AI script from Icewind Dale: Enhanced Edition.

--

Script components:
-

1. **Better IWD Pregen**
	- Adds 3-4 party AI scripts (d2scrp, d2scrp+, d2scrp-, iwdpgen)
 	- More info below
2. **Better AI for Call Woodland Beings (EEs, BG2)**
	- Option 1: Use revised script for nymph summon (compatible with SCS)
	- Option 2: Use existing script, but patch in a few actions (use with revision mods)
	- Note: This component needs to be installed after AI mods (ex. SCS or atweaks)
3. **Auto-assign script to new characters**
	- Can choose any of the 3-4 scripts from this mod

--

Tweak components:
-

1. **Adjust enemy damage at higher difficulties (IWD1, IWD2)**
	- IWD2: includes exe patch by Bubb (required for damage adjust to work)
2. **Add or remove Avarine Decanter (IWD2)**
	- Won't cause issues if the item is already obtainable
3. **Unnerf Animate Dead (IWD2)**
	- Also corrects chance of each summon to 50/50
	- This is skipped if IWD2EE "Spell Revisions" is installed
4. **Shapeshift movement bonuses bypass Free Action (EEs)**
	- Can set to bypass or be blocked by Free Action
5. **Increase movement speed of IWD shapeshifts (IWD1, IWDEE)**
	- EEs: increases Polar Bear and Winter Wolf movement
	- classic: increases all forms (most are still slower than natural form)  

--

6. **Give party starting equipment (IWD games)**
	- Option 1: Items are auto-equipped or added to inventory
	- Option 2: Start with a bag, containing a mix of weapons (choose this if using a Proficiencies overhaul)
7. **Give party a Bag of Holding at game start (classic and EEs)**
	- Option 1: "Bottomless" bag (same as Tweaks Anthology component)
	- Option 2: Capacity = 50 items (IWD2 default)
	- Option 3: Capacity = 100 items (BG2 default)
	- Option 4: Bottomless, and Gold is exchanged when adding/removing items (EE-only)
8. **All classes get full HP bonuses from Constitution (classic and EEs)**
	- Option 1: 2e-style HP bonuses (i.e. BG-style)
	- Option 2: 3e-style bonuses (+1 or -1 every 2 Con) (WARNING: Prism will spawn dead in BG1.)
	- Option 3: Mixed (use 3e-style at 10+, normal BG penalties at under 10)
	- Note: Does not overwrite any previous changes to Con effects, except for HP bonus
9. **Reduce delay for Sneak Attacks + uncap Crippling Strike (EEs)**
	- Can set delay to 1 round or 5 rounds (stat reduction does not stack)
	- Note: Crippling Strike is capped at -7 stat reduction in unmodded IWDEE
10. **Salamander auras hit only enemies of the caster (IWDEE)**
	- Can patch just Avenger form or enemy auras as well
	- Can optionally make Cloudburst party friendly  

--

11. **Misc spell tweaks (classic and EEs):**
	- Damage party friendly (relative to caster)
	- Hit stun on damage (1 second)
	- No mage school restrictions
	- Note: There are multiple options. You can install all, 1 tweak, or any combo of 2.
12. **Allow Minsc to use his Berserk ability at will (BG games)**
	- Options to set duration to 5 rounds, 1 turn, or 2 turns
13. **Patch visuals for shortbows (IWDEE) or scimitars (IWD-in-BG2)**
	- IWDEE: makes shortbows look like shortbows in the inventory screen
	- IWD-in-BG2: makes scimitars look like scimitars (instead of long sword)
14. **Remove alignment restrictions for classes (classic and EEs)**
	- This patches any mod-added kits as well, including multiclass kits
	- Has options to skip certain classes (paladins, clerics, monks, etc.)
15. **Prevent paladins and rangers falling at low rep (EEs)**
	- This patches any mod-added kits as well
	- Can optionally install for only rangers or only paladins

--

**Additional info:**
- All components can be installed independently and in any order, except for auto-assigning the script.
- All components should be safe to install at end-of-order. If another mod says to install last, you can try it both ways.
- If using tweaks from other mods that do similar things, whichever is installed last will usually be used.
- All tweaks have at least 2 subcomponents. i.e. if you say to "install all components", it won't automatically install any tweaks.

Scroll down for additional info on some of the tweaks.

---
---

# Overview (party script):

This script manages auto-attack, while giving more nuanced control of the characters. The script will never use your consumable items, spells, or abilities. The main aim is to (hopefully) reduce some of the more frustrating aspects of auto-attack.

#### Script - Quick Info:
- Better IWD Pregen (d2scrp): Base script. Includes all features listed below.
- d2scrp+: Same as base script, except calls for help are enabled.
- d2scrp-: Same as base script, except default mode is Cooldown.
- IWD Pregen (iwdpgen): Same as vanilla IWD Pregen, but with shaman abilities added. (EE-only)

#### Auto-attack features:
- Melee aggro range is dependent on class (see below for full breakdown); range from 5 ft. (mages) to 27 ft..
- Will not attack if under the effects of Invisibility or Sanctuary.
- Will not attack if using Stealth, Bard Song, Turn Undead or Shamanic Dance.
- EEs: Active retargeting if a character's current weapon cannot hit or damage an enemy.
- Priority targeting against enemy casters (limited to within 5 ft. or in range of current weapon).
- Cooldown hotkeys to reduce melee aggro range to 5 ft. for 30 seconds, or set back to normal instantly.

#### Other features:
- Classes with Search will use it when not attacking (note: for IWD2, auto-Search only works if a character has Rogue or Monk levels).
- Will not auto-Search if using Stealth, Bard Song, Turn Undead or Shamanic Dance.
- Will attempt to stop attacking, or stop a Bard Song, if suddenly invisible (ex. from a contingency or area invisibility spell).
- Shamanic Dance is NOT stopped if suddenly invisible. This is to preserve summons.
- Will not auto-attack at under 15% HP, unless an enemy is in range of current weapon.

#### Cooldown hotkeys:
- If the B key is pressed, the character will enter a Cooldown mode for 30 seconds.
- Cooldown reduces melee aggro range to 5 ft. and disables some of the retargeting actions.
- If the E key is pressed, the Cooldown mode will be deactivated.
- If the game is saved while a character is in Cooldown mode, it will be deactivated on reload.

Note: Stealth, Bard Song, Turn Undead and Shamanic Dance will prevent any Cooldown-related actions from triggering.

--

Additional info:
-
<details>
  <summary>Script Compatibility</summary>

Script Compatibility:
-

- EEs: BG:EE, BG2:EE, IWD:EE, EET (tested on v2.5/v2.6)
- Classic: BG1, BG2, IWD, IWD2 (tested with GOG versions)

Also compatible with any BG2 conversion mods (ex. BGT or Classic Adventures).

#### Classic BG2 engine:  
- TobEx (v26/v28): Compatibility issues should be fixed (v3.7 and later).  
- TobEx Afterlife: Use v29.10 or later. (http://www.shsforums.net/files/file/1274-tobex-afterlife)  
- Improved GUI mod: Use v5.1 or later. (http://www.shsforums.net/files/file/1265-bg2-improved-gui)

NOTE: I'm not 100% sure the scripts work with expansionless versions of the classic games.
  
--

</details>

<details>
  <summary>Auto-attack breakdown</summary>

Auto-attack breakdown
-

**BG(EE), BG2(EE), IWD(EE):**

  ```
Class: Fighter, Ranger, Paladin, including any multiclass combinations
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 27 ft.
	3. Attacked by enemy

Class: Kensai, Monk, Shapeshift/Polymorph (without Fighter levels)
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 19 ft.
	3. Attacked by enemy

Class: Cleric, Druid, Shaman, Thief, Bard, Cleric/Thief
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 13 ft.

Class: Mage, Sorcerer, Mage/Thief, Cleric/Mage
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 5 ft.
	3. If THAC0 is less than 5, will attack if enemy is within 13 ft.
  ```

 --

**IWD2:**

  ```
Class: Fighter, Ranger, Paladin or Barbarian (single-class or multiclass with 3+ levels)
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 27 ft.
	3. Attacked by enemy

Class: Monk (Level 9+), Wild Shape/Tenser's/Iron Body (without 3+ warrior levels)
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 19 ft.
	3. Attacked by enemy

Class: Cleric, Druid, Monk, Thief or Bard, including multiclass with Wizard or Sorcerer
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 13 ft.

Class: Wizard or Sorcerer
	Conditions (one must be met to auto-attack)
	1. Enemy is within range of the currently equipped weapon
	2. Enemy is within 5 ft.
  ```
  
--

</details>

<details>
  <summary>Nymph AI script (Call Woodland Beings)</summary>

Nymph AI script (Call Woodland Beings)
-

**Option 1 - Revised script:**
- Smarter spellcasting (better targeting, checks magic resist, etc.).
- May cast Barkskin, Mass Cure, Entangle, or Summon Insects once each per combat encounter. When the AI uses these spells, it doesn't require or consume any memorized spells.
- Slightly increased movement and casting speed.
- Teleports to catch up with the party (ex. while traveling with Boots of Speed).
- Preserves invisibility (won't attack or cast spells).
- Cooldown hotkeys to delay spellcasting (B to enable, E to disable).

Compatible with EEs and classic BG2 engine, including SCS.  
Not compatible with atweaks PnP Fey (use option 2).

--

Dimension Door: The nymph can teleport if conditions are met. It will alway teleport to either the nearest enemy or to a PC (usually, its summoner). It will not use Dimension Door if invisible, unless instructed to by the player (with the D key).

Marking: The nymph "marks" a PC as an object for various actions (by default, this is the summoner). If the marked PC is not on the map for any reason, the nymph will choose another PC on the same map. The nymph will always switch back to its summoner if in visual range. Note that the summoner, as an identifier, is not saved if a summon is still on the map (so if reloading, script will default to Player1 as the "marked" PC).

--

**Hotkeys:**
- If the D key is pressed the nymph will teleport to its summoner (or other PC). Only works when not in combat.
- If the B key is pressed, the nymph will enter Cooldown for 3 rounds. Cooldown mode disables most combat actions.
- If the E key is pressed, the Cooldown timer is set to 0 (deactivated).

--

**Option 2 - Patch existing script:**
- Adds Cooldown hotkeys (B to enable, E to disable)
- Adds D hotkey to teleport to party (out of combat only)
- Teleports to party if not in visual range (and not invisible)
- Preserves invisibility (won't attack or cast spells)
- Usable with atweaks PnP Fey, as well as AI mods that still use NYMPH.BCS (ex. SCS)

NOTE: Dimension Door is more limited with this patch. Will only teleport to the summoner or Player1.
  
--

</details>

<details>
  <summary>Baldur's Gate (original BG1 engine)</summary>

Baldur's Gate (original BG1 engine)
-

- Characters will preserve Hide/Invisibility/Sanctuary
- Melee aggro ranges working
- Calls for help working (d2scrp+)
- Cooldown hotkeys working
- No auto-Search (the FindTraps() script action doesn't work)

NOTE: Bard Song and Turn Undead won't prevent auto-attacking, but you can keep them active during battle if the character is standing outside melee aggro range (obviously with a melee weapon equipped)
  
--

</details>


---
---


# Tweaks info

<details>
  <summary>Adjust enemy damage at higher difficulties (classic IWD, IWD2)</summary>

Adjust enemy damage at higher difficulties (classic IWD, IWD2)
-

- The party normally takes 2x damage on Insane/HoF (or 1.5x on Very Hard).
- This component removes the damage bonus by setting this option in the game INI:

> Suppress Extra Difficulty Damage=1

NOTE: For IWD2, this setting doesn't work in the unmodded game. Thanks to an exe patch by Bubb, the option can be enabled. This patch is included with Bubb's permission.
  
--

</details>

<details>
  <summary>Unnerf Animate Dead (IWD2)</summary>

Unnerf Animate Dead (IWD2)
-

- The nerfed version caps at the Level 9 summons.
- Also corrects the chance of each creature type to 50/50 (was 51/49).
- Skipped if the IWD2EE "Spell Revisions" component is installed.

--

**Level - Summons**
- 1 - Skeleton, Skeleton Archer, Zombie
- 5 - Armored Skeleton, Chosen Zombie
- 7 - Boneguard Skeleton, Poison Zombie
- 9 - Greater Boneguard, Zombie Lord
- 11 - Cold Bones, Greater Zombie Lord
- 13 - Elite Greater Boneguard, Greater Drowned Dead
- 15 - Barrow Wight, Mummy King
- 17 - Apocalyptic Boneguard, Festering Drowned Dead

--

**NOTE: Festering Drowned Dead emits an aura, affecting living creatures, with several possible negative effects (including instant death) on a failed save vs. Fortitude. The aura prevents saving the game while active.**

You can also unnerf this spell by deleting SPWI501.SPL from the override.
  
--

</details>

<details>
  <summary>Increase movement speed of IWD shapeshifts (IWD1, IWD:EE)</summary>

Increase movement speed of IWD shapeshifts (IWD1, IWD:EE)
-

IWDEE:
- Increases movement of polar bear and winter wolf forms. 
- Winter wolf will move slightly faster than in natural form.
- Polar bear is similar speed or slightly slower (depending on angle of movement).

IWD1 (classic):
- Increases movement of all Druid shapeshifts. 
- The winter wolf moves faster than in natural form. 
- Polar bear gets a huge increase. It now moves similar speed to natural form (instead of ridiculously slow).
- The boring beetle and elementals are slightly slower than natural form.

Additional info:
- There are no conflicts with this tweak and the similar tweak in my [Polymorph fixes](https://github.com/D2-mods/Polymorph-fixes-for-IWDEE) mod. If differing options are chosen, the game will use whichever is installed last.
- Classic IWD: The 2 installer options are identical. Game doesn't have a polymorph spell.
  
--

</details>

<details>
  <summary>Give party starting equipment (IWD games)</summary>

Give party starting equipment (IWD games)
-

This component gives the party basic starting weapons, as well as the "Worn Garment" armor. Weapons are given based on proficiencies (IWDEE), or class (IWD2), or randomly (classic IWD). There's also an option to start with a bag, containing at least 1 of each weapon type. More info below.

- Note: For IWD2, the pre-made parties already start out equipped, so this just makes it more fair for custom parties.  
- This component is fully compatible with the IWD2EE mod. It's also compatible with IWD-in-BG2, if you really want to use that version.

--

**Scripting notes:**

This is a global script that runs once per character slot per game. If the character exists, the script will start for that slot. It specifically looks for a quarterstaff in the inventory (which level 1 characters will always start with). It will not give starting items if already equipped (i.e. you imported a character from a previous playthrough).

After about 1 round, the script will never run again for that playthrough for that character slot.

--

**Option 1 (auto-equip):**

How it works:
- Start a new game with new characters (you can also load one saved at the start).
- Wait a few seconds for the script to run for each character.
- That's it. The items will be either equipped or in the inventory.
- For classic IWD, you may need to open/close the Inventory screen 1-2 times to make the script run.

**NOTE: Auto-equip option is not compatible with proficiency overhauls.**


<details>
  <summary>Additional info:</summary>

--

**IWDEE:**
- Items are created based on a character's proficiencies (up to 1 melee and 1 ranged).
- Characters with no melee profs will keep the starting staff.
- Weapons are added to the quickslots or inventory.
- No known issues.

--

**Classic IWD:**
- This game doesn't have a way to detect proficiencies from a script.
- The party receives a randomized set of items (a few items are non-random).
- Total amount of items received is based on size of the initial party.
- For organization, all weapons will be in the inventories of Player1 or Player2.
- Characters will keep the starting staff (removing it can lead to a possible crash).

--

**IWD2:**
- This game doesn't have a way to detect Feats from a script.
- Each character receives one melee and one ranged weapon.
- Items are slightly randomized. Possible items are based on character class.
- Weapons are moved to the quickslots, but are NOT auto-equipped.
- Do one of the following to equip weapons:
	- Save and reload
	- Open and exit Character arbitration
	- Pick up and re-equip each weapon

--

**IWD-in-BG2:**
- Works the same as in IWD:EE.
- Quickslot icon is not automatically updated.
- To update the icon, pick up and re-equip each weapon (save/reload doesn't work).

--

</details>

--

**Option 2 (weapon bag):**

This component will give the party a bag, containing a selection of weapons. A single bag is given and the player can choose what to do with unwanted items (i.e. sell or throw away). The contents is the same regardless of party size. The bag contains at least one of each weapon type, so it should be compatible with any Proficiencies overhauls.

NOTE: If the separate "Give party a Bag of Holding" component is not installed, then items can only be taken out of the weapon bag. If it is installed, then the bag is changed to a normal Bag of Holding.
  
--

</details>

<details>
  <summary>Give party a Bag of Holding at game start (classic and EEs)</summary>

Give party a Bag of Holding at game start (classic and EEs)
-

- The first 3 options give a Bag of Holding with differing max capacities. 
- The "Bottomless" option has a capacity of 32767 items, same number used by Tweaks Anthology.
- Compatible with all IE games that support Bags of Holding (except PsT:EE for now).

--

**Option 4 (EEs) - Bottomless, and Gold is exchanged when adding/removing items (experimental)**

You start with a bottomless bag (60000+ capacity), but unlike other bags, gold is added or taken away whenever items are transferred. Otherwise, it works like a regular bag.

v7.14 changes:
- BGEE/BG2EE have 65% resell and 140% markup if buying back.
- IWDEE/PSTEE have 80% resell and 130% markup if buying back.
- previously, all games had 65% resell and 180% markup.


<details>
  <summary>Additional info (Option 4):</summary>

--

**Notes:**
- Bag screen doesn't show current gold amount (except in PSTEE).
- You can sell items in the bag to merchants. (still costs gold to remove from bag)
- Reputation has no effect.
- Charisma of the active character (the one with the bag) adjusts price for buying items back.

NOTE: Items cannot be taken out of the bag if party lacks the gold to buy it back.

--

**Issues/Exploits:**
- Rechargeable items: Gold gained when putting in the bag is always the same (current charges doesn't matter). Removing an item, however, costs less with fewer charges. At 0 charges, an item is actually free to take out. So you can deplete an item of charges, then continually add and remove it to make infinite gold.
- Items with 1 gold base price will give 0 gold when putting in the bag.

--

</details>
  
--

</details>

<details>
  <summary>Reduce delay for Sneak Attacks + uncap Crippling Strike (EEs)</summary>

Reduce delay for Sneak Attacks + uncap Crippling Strike (EEs)
-

Reduce delay for Sneak Attacks:
- Default delay is 420 seconds (i.e. immunity effect on target).
- Options to reduce delay to 6 or 30 seconds, or keep unchanged.
- 3rd option (no change) will patch effects if a related tweak from OlvynTweaks is detected.

Uncap Crippling Strike:
- Allows Crippling Strike to scale to -16 (Assassin at level 50).
- By default, the stat reduction is capped at -7 (EE v2.5 and v2.6.6).
- The dialogue box and Record screen could show higher numbers, but the effect never went past -7.
- Main purpose is to allow Assassins to reach -10 in IWD:EE.
  
--

</details>

<details>
  <summary>Misc spell tweaks (classic and EEs)</summary>

Misc spell tweaks (classic and EEs)
-

- This has 3 tweaks:
	- Damage party friendly (relative to caster)
	- Hit stun on damage (1 second)
	- No mage school restrictions
- Safe to install at end-of-order. Install after any mods that adds spells or items.
- It has multiple subcomponents. You can install all tweaks, just 1 tweak, or any combo of 2.
- The damage ones will also check item spells (wands, potions, etc.).

--

**Additional info (spell tweaks):**
- The damage tweaks ignore poison, disease, and other hardcoded damage effects.
- The damage tweaks ignore spells that target the caster with no projectile (ex. self-damage from berserker Enrage)
- The damage tweaks ignore most subspells. (note: installer will always check SPLs with long range or an offensive "secondary type")
- "No mage school restrictions" is both a tweak and a workaround for a serious issue with sorcerer kits (spell schools missing from selection screen). More info in this post at G3 forums: https://www.gibberlings3.net/forums/topic/36181-spell-selection-issue-sorcererscharacter-creation/#comment-318196
- "No mage school restrictions" will also make all arcane scrolls usable by any specialist. (note: Making the spell appear in the selection screen also makes the "Write Magic" button appear, even if scroll is unusable).
- Hit stun note: Does not remove any stun effects already on the spell, so longer durations will still be there.
- Hit stun note: Applies only once per spell. (ex. Melf's arrow stuns only on initial hit.)
- Hit stun note: For spells with saving throws for half damage, stun is only if save is failed.
- Hit stun note: skips repeating area damage (ex. Cloudkill). Similar mod spells are skipped if Secondary type is set to BATTLEGROUND.
- Hit stun note: skips counter/barrier spells (Fire Shield, Blade Barrier, etc.). Similar mod spells are skipped if Secondary type is set to any PROTECTIONS type.

--

**Game-specific info:**
- PSTEE: "No mage school restrictions" not available. (note: many PSTEE spells use hardcoded projectiles or effects, so the damage ones only apply to a few spells)
- BG1 (classic): "Damage party friendly" not available.
- IWD1/IWD2 (classic): Projectiles that apply damage directly are skipped for damage tweaks (ex. Agannazar's Scorcher). Most spells like fireball, skull trap, etc. will be patched. If unsure, test spell on PCs before using.
- IWD1 (classic): "Damage party friendly" does not reliably protect from wands/item spells unless they are casting an actual spell. Most wands apply effects directly instead of casting a spell.
- IWD2: "No mage school restrictions" will change all arcane spells to Generalist school. This is the only way to make it work for IWD2. This means that bonuses from feats or other sources will not apply. (note: Specialists will still have a bonus spell slot and will still be identified as the specialist for scripts and dialogues.)

--

</details>

<details>
  <summary>Allow Minsc to use his Berserk ability at will (BG games)</summary>

Allow Minsc to use his Berserk ability at will (BG games)
-

- Can set duration to 30, 60, or 120 seconds.
- The way it works differs by game:
	- EEs: Can be recast at any time (stat bonuses do not stack).
	- BG1: Regain ability after duration runs out.
	- BG2: Regain ability immediately, but cannot recast until duration runs out.
- BG2EE: Fixes a timing error, which caused Minsc to always take damage when the ability ended, even at full health.
- BG2: Fixes incorrect durations for some effects (tested in BG2 fixpack v13)

NOTE: Will be skipped if Rashemi Berserker (Artisan's Kitpack) is installed
  
--

</details>

<details>
  <summary>Patch visuals for shortbows (IWD:EE) or scimitars (IWD-in-BG2)</summary>

Patch visuals for shortbows (IWD:EE) or scimitars (IWD-in-BG2)
-

- IWDEE: Patch shortbows to use shortbow appearance (as in classic IWD)
- IWD-in-BG2: Patch scimitars to use scimitar appearance (was using long sword)

NOTE: Shortbow appearance can't be set for IWD-in-BG2
  
--

</details>

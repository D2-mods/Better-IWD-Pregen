==================================================
Adjust enemy damage at higher difficulties (classic IWD, IWD2)
==================================================
- The party normally takes 2x damage on Insane/HoF (or 1.5x on Very Hard).
- This component removes the damage bonus by setting this option in the game INI:

Suppress Extra Difficulty Damage=1

NOTE: For IWD2, this setting doesn't work in the unmodded game. 
      Thanks to an exe patch by Bubb, the option can be enabled. 
      This patch is used with Bubb's permission.


==================================================
Add or remove Avarine Decanter (IWD2)
==================================================
- This component adds or hides this item from the seller's store.
- Official patches added the other bonus items, but not this one.
- GOG version includes it by default.


==================================================
Unnerf Animate Dead (IWD2)
==================================================
- This is a patching component. Should be safe to install after spell tweaks.
- The nerfed version caps at the Level 9 summons.
- Mages and Clerics both use SPWI501.SPL (the similar spell SPPR301.SPL exists, but is unused).
- Also corrects the chance of each creature type to 50/50 (was 51/49).

Level - Summons
1 - Skeleton, Skeleton Archer, Zombie
5 - Armored Skeleton, Chosen Zombie
7 - Boneguard Skeleton, Poison Zombie
9 - Greater Boneguard, Zombie Lord
11 - Cold Bones, Greater Zombie Lord
13 - Elite Greater Boneguard, Greater Drowned Dead
15 - Barrow Wight, Mummy King
17 - Apocalyptic Boneguard, Festering Drowned Dead

NOTE: Festering Drowned Dead emits an aura, affecting living creatures, 
with several possible negative effects (including instant death) on a failed 
save vs. Fortitude. The aura prevents saving the game while active.

You can also manually unnerf this spell by deleting SPWI501.SPL from the override.


==================================================
Shapeshift movement bonuses bypass Free Action (EEs)
==================================================
This lets you set all movement bonuses from shapeshifts to bypass Free Action, or be blocked by Free Action. Note that a Free Action applied afterwards can still reset movement rate back to the base value. This component will also set all movement bonuses to the stacking multiplier. The EEs, especially IWD:EE, are inconsistent with these effects, and there are also differences between EE v2.5 and v2.6.

This component is similar to the one in my Polymorph fixes mod for IWD:EE, except it applies also to the BG:EE games. There are no known issues if installed together. If differing options are chosen, the game will use whichever is installed last.


==================================================
Increase movement speed of Winter Wolf and Polar Bear forms (IWD:EE)
==================================================
This is something I decided to add while testing the AI script in classic IWD1. The winter wolf form in the original moves noticeably faster than the IWD:EE version. This isn't boots of speed fast, but it's a little faster than in human form. The bear is painfully slow in all versions of the game, but I don't think a speed increase is overpowered. It's still inferior to the Boring Beetle's high defenses.

NOTE: This component will also remove the erroneous Haste effect from the Polymorph Self versions of the Druid animals (with wolf and bear forms getting the movement bonus instead).

This component is 100% identical to the one in my Polymorph fixes mod, but they are safe to install together. If differing options are chosen, the game will use whichever is installed last.


==================================================
Give party starting equipment (IWD games)
==================================================
This component gives player characters basic starting weapons, because my characters aren't idiots who travel to Icewind Dale unprepared. For IWD2, the pre-made parties already start out equipped, so this just makes it more fair for custom parties.

This is a global script that runs once per character per game.


Component 1 (auto-equip)

Instructions:
- Start a new game with new characters (you can also load one saved at the start).
- Wait a few seconds for the script to run for each character.
- That's it. The items will be either equipped or in the inventory.
- For classic IWD, you may need to open/close the Inventory screen 1-2 times to make the script run.

NOTE: Auto-equip option is not compatible with proficiency overhauls.


Additional info:
----------------------------------------------------------------------------------------------------
IWD:EE
- Items are created based on a character's proficiencies (up to 1 melee and 1 ranged).
- Characters with no melee profs will keep the starting staff.
- Weapons are added to the quickslots or inventory.
- No known issues.

Classic IWD
- This game doesn't have a way to detect proficiencies from a script.
- The party recieves a randomized set of items (a few items are non-random).
- Total amount of items recieved is based on size of the initial party.
- For organization, all weapons will be in the inventories of Player1 or Player2.
- Characters will keep the starting staff (removing it can lead to a possible crash).

IWD2
- This game doesn't have a way to detect Feats from a script.
- Each character recieves one melee and one ranged weapon.
- Items are slightly randomized. Possible items are based on character class.
- Weapons are moved to the quickslots, but are NOT auto-equipped.
- Do one of the following to equip weapons:
	- Save and reload
	- Open and exit Character arbitration
	- Pick up and re-equip each weapon

IWD-in-BG2
- Works the same as in IWD:EE.
- Quickslot icon is not automatically updated.
- To update the icon, pick up and re-equip each weapon (save/reload doesn't work).
----------------------------------------------------------------------------------------------------

Component 2 (weapon bag)

This component will give the party a bag, containing a selection of weapons. A single bag is given and the player can choose what to do with unwanted items (i.e. sell or throw away). The contents is the same regardless of party size. For IWDEE, the bag contains at least one weapon from each BG2 proficiency, so it should be compatible with proficiency overhauls.

NOTE: If the separate "Give party a Bag of Holding" component is not installed, then items can only be taken out of the weapon bag. If it is installed, then the bag is changed to a normal Bag of Holding. You only have one bag with both installed, and install order doesn't matter.


==================================================
Give party a Bag of Holding at game start (classic and EEs)
==================================================
The first 3 components give a Bag of Holding with differing max capacities. 
The "Bottomless" option has a capacity of 32767 items, same number used by Tweaks Anthology.
Compatible with all IE games that support Bags of Holding (except PsT:EE for now).


Option 4 (EEs) - Bottomless, and Gold is exchanged when adding/removing items (experimental)
----------------------------------------------------------------------------------------------------
You start with a bottomless bag (60000+ capacity), but unlike other bags, gold is added or taken away whenever items are transferred. Otherwise, it works like a regular bag.

Note that taking items out of the bag isn't cheap. I set to a 180% markup, so comparable to the more expensive merchants. However, the gold you get for putting items into the bag is higher than what you'd get from most stores, and there's no depreciation. In BG2, the amounts are comparable to the best ToB merchants. In IWD, there are several merchants that will pay more, but most will only accept certain item types.


Additional info:
- Bag screen won't show any numbers (for current gold or amounts transferred).
- You can sell items in the bag to merchants (still costs gold to remove from bag).
- Reputation has no effect.
- Charisma of the active character (the one with the bag) adjusts price for buying items back.

NOTE: Items cannot be taken out of the bag if party lacks the gold to buy it back.

Issues/Exploits:
- Rechargeable items: Gold gained when putting in the bag is always the same (current charges doesn't matter). Removing an item, however, costs less with fewer charges. At 0 charges, an item is actually free to take out. So you can deplete an item of charges, then continually add and remove it to make infinite gold.
- Items with 1 gold base price will give 0 gold when putting in the bag.
----------------------------------------------------------------------------------------------------


==================================================
All classes get full HP bonuses from Constitution (classic and EEs)
==================================================
- Choice between 2e/BG-style, or the more even HP curve of later editions.
- Usable with all versions of BG1, BG2, and IWD, including conversion mods.


==================================================
Fixes for backstab-related 2DA files (EEs)
==================================================
- Fixes problematic lines in backstab-related 2das (added by some mod kits).
- Also makes sure base-game kits have correct progression to level 40 or 50.
- Will also add all files necessary for Sneak Attack (if missing).


==================================================
Reduce delay for Sneak Attacks + uncap Crippling Strike (EEs)
==================================================
Reduce delay for Sneak Attacks
- Default delay is 420 seconds (i.e. immunity effect on target).
- Options to reduce delay to 6 or 30 seconds, or keep unchanged.
- 3rd option (no change) will patch effects if a related tweak from OlvynTweaks is detected.

Uncap Crippling Strike
- Allows Crippling Strike to scale to -16 (Assassin at level 50).
- By default, the stat reduction is capped at -7 (EE v2.5 and v2.6.6).
- The dialogue box and Record screen could show higher numbers, but the effect never went past -7.
- Main purpose is to allow Assassins to reach -10 in IWD:EE.


==================================================
Allow Minsc to use his Berserk ability at will (BG games)
==================================================
- Can set duration to 30, 60, or 120 seconds.
- The way it works differs by game:
	- EEs: Can be recast at any time (stat bonuses do not stack).
	- BG1: Regain ability after duration runs out.
	- BG2: Regain ability immediately, but cannot recast until duration runs out.
- BG2EE: Fixes a timing error, which caused Minsc to always take damage when the ability ended, even at full health.
- BG2: Fixes incorrect durations for some effects (tested in BG2 fixpack v13)

NOTE: Will be skipped if Rashemi Berserker (Artisan's Kitpack) is installed


==================================================
Patch visuals for shortbows (IWD:EE) or scimitars (IWD-in-BG2)
==================================================
- IWDEE: Patch shortbows to use shortbow appearance (as in classic IWD)
- IWD-in-BG2: Patch scimitars to use scimitar appearance (was using long sword)

NOTE: Shortbow appearance can't be set for IWD-in-BG2


==================================================
Remove alignment restrictions for classes (classic and EEs)
==================================================
- All classes can be any alignment
- Affects all kits as well, including mod kits


==================================================
Paladins and Rangers do not fall at low rep (EEs)
==================================================
- No falling at low rep
- Affects all kits as well, including mod kits



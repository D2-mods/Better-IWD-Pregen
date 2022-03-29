==================================================
Adjust enemy damage at higher difficulties (IWD1)
==================================================
- be default, your characters take 2x damage on Insane/HoF (or 1.5x on Very Hard, which no one uses)
- you usually end up relying on summons or cheap tactics like abusing invisibility
- this component removes the damage bonus by setting this option in the game INI:

Suppress Extra Difficulty Damage=1

NOTE: IWD2 has a similar INI option, but I couldn't get it to work. The game resets it to 0 when loading a game or opening the Options menu.


==================================================
Avarine Decanter (IWD2)
==================================================
- this component adds or hides this item from the seller's store
- allows you to obtain some useful items relatively early
- GOG version includes it by default
- official patches added the other bonus items, but not this one


==================================================
Animate Dead (IWD2)
==================================================
- this is a patching component; should be safe to install before or after any spell tweaks
- nerfed version caps at the Level 9 summons
- Clerics also use SPWI501.SPL (the similar spell SPPR301.SPL exists, but is unused)
- also corrects the chance of each creature type to 50/50 (was 51/49)

Level - Summons
1 - Skeleton, Skeleton Archer, Zombie
5 - Armored Skeleton, Chosen Zombie
7 - Boneguard Skeleton, Poison Zombie
9 - Greater Boneguard, Zombie Lord
11 - Cold Bones, Greater Zombie Lord
13 - Elite Greater Boneguard, Greater Drowned Dead
15 - Barrow Wight, Mummy King
17 - Apocalyptic Boneguard, Festering Drowned Dead

NOTE: Festering Drowned Dead emits an aura, affecting living creatures, with several possible negative effects (including instant death) on a failed save vs. Fortitude. The aura prevents saving the game while active.

You can also manually unnerf this spell by deleting SPWI501.SPL from the override.


==================================================
Shapeshift - movement bonus patch (EEs)
==================================================
This lets you set all movement bonuses to bypass Free Action, or be blocked by Free Action. Note that a Free Action applied afterwards can still reset movement rate back to the base value. This component will also set all movement bonuses from polymorphs to the stacking multiplier. The EEs, especially IWD:EE, are inconsistent with these effects, and there are also difference between EE v2.5 and v2.6.

This component is similar to the one in my Polymorph fixes mod for IWD:EE, except it applies also to the BG:EE games. There are no known issues if installed together. If differing options are chosen, the game will use whichever is installed last.


==================================================
Winter Wolf and Polar Bear speed (IWD:EE)
==================================================
This is something I decided to add while testing my AI script in classic IWD1. The winter wolf form in the original moves noticeably faster than the IWD:EE version. This isn't boots of speed fast, but it's a little faster than in human form. The bear is painfully slow in all versions of the game, but I don't think a speed increase is overpowered. It's still inferior to the Boring Beetle's high defenses.

NOTE: This component will also remove the erroneous Haste effect from the Polymorph Self versions of the Druid animals (with wolf and bear forms getting the movement bonus instead).

This component is 100% identical to the one in my Polymorph fixes mod, but they are safe to install together. If differing options are chosen, the game will use whichever is installed last.


==================================================
Give party starting equipment (IWD games)
==================================================
This component gives player characters basic starting weapons, because my characters aren't idiots who travel to Icewind Dale unprepared. The pre-made parties in IWD2 also start out equipped, so this just makes it more fair for custom parties.

This is a global script that runs once per character per game. It can theoretically take effect for games that are already started, but unless you're still at the beginning, you should have better equipment already.

NOTE: For IWDEE, if using a proficiency overhaul mod, component 2 should usually be chosen, as the scripts for component 1 do not currently adjust for other mods.


Component 1 (auto-equip)

Instructions:
- after installing, start a new game with new characters (you can also load one saved at the start)
- wait a few seconds for the script to run for each character
- that's it, the items will be either equipped or in the inventory
- for classic IWD, if loading an existing save, you may need to open/close the Inventory or Record screen 1-2 times to make the script run

Info/Known issues:

IWD:EE
- items are created based on proficiencies
- characters with no melee proficiencies will keep the starting quarterstaff
- weapons are added to the quickslots, though some are intentionally left in the inventory
- no known issues

IWD1
- this game doesn't have a way to detect proficiencies in a script trigger
- the party recieves a randomized set of items (a few items are non-random)
- total amount of items recieved is based on size of the initial party
- for organization, all weapons will be in the inventories of Player1 or Player2
- characters will also keep the starting staff (removing it can lead to a possible crash)

IWD2
- this game doesn't have a way to detect Feats in a script trigger
- each character recieves one melee and one ranged weapon
- items are slightly randomized and based on character class
- weapons are moved to the quickslots, but are not auto-equipped
- saving/reloading will properly equip them, as will manually picking up and re-equipping the weapons

IWD-in-BG2
- works the same as in IWD:EE
- quickslot icon (in main game screen) is not auto-updated
- to update the icon, pick up and re-equip each weapon (save/reload doesn't work)


Component 2 (weapon bag)

This component will give the party a bag, containing a selection of weapons. A single bag is given and the player can choose what to do with unwanted items (i.e. sell or throw away). The contents is the same regardless of party size. For IWDEE, the bag contains at least one weapon from each BG2 proficiency, so it should be compatible with any proficiency overhauls.

NOTE: If the separate "Give party a Bag of Holding" component is not installed, then items can only be taken out of the weapon bag. If it is installed, then the bag is changed to a normal Bag of Holding. You only have one bag with both installed, and install order doesn't matter.


==================================================
Give party a Bag of Holding (classic and EEs)
==================================================
This is pretty self-explanatory. You start the game with a bag. The first 3 components just give a Bag of Holding with differing max capacities. The "Bottomless" option has a capacity of 32767 items, same number used by Tweaks Anthology.

Compatible with all IE games that support Bags of Holding (except PsT:EE for now).


The 4th option is experimental and EE-only. You start with a bottomless bag (60000+ capacity). But unlike other bags, gold is added or taken away whenever items are added or removed. It works like a store, but I cut out the middleman entirely. You just put items in, or take them out, like a regular bag.

Note that taking items out of the bag isn't cheap. I have it set to 180% markup, so comparable to the more expensive merchants. However, the gold you get for putting items into the bag is higher than what you'd get from most stores, and there's no depreciation. In BG2, the amounts are comparable to the best ToB merchants. In IWD, there are several merchants that will pay more, but most will only accept certain item types.


Additional info:
- bag screen won't show any numbers, you'll need to check the gold amount in the inventory
- Reputation has no effect on this bag/store
- Charisma of the active character (the one with the bag) adjusts price for buying items back
- items with 1 gold base price will always give 0 gold when putting in the bag
- items with 0 gold base price are free to transfer either way (ex. regular arrows)

Issues/Exploits:
- Items in the bag can still be sold to merchants (so basically get double sell price).
- Rechargeable items: Amount gained when putting in the bag is always the same (charges left doesn't matter). Removing the item, however, seems to take into account the current charges. At 0 charges, an item is actually free to take out. So the exploit is obvious. You can deplete an item of charges, then continually add and remove it from the bag to make infinite gold. Resting will recharge any items in the bag.


==================================================
All classes get full HP from CON (classic and EEs)
==================================================
- yet another universal CON bonus mod
- choice between 2e/BG-style, or the more even HP curve of later editions
- usable with all versions of BG1, BG2, and IWD, including conversion mods


==================================================
Misc fixes for backstab-related 2DA files (EEs)
==================================================
- fixes problematic lines in backstab-related 2das (added by some mod kits)
- also makes sure base-game kits have correct progression to level 40 or 50
- will also add all files necessary for Sneak Attack (if missing)


==================================================
Sneak Attack tweak + Crippling Strike fix (EEs)
==================================================
Reduce delay for Sneak Attacks
- default delay is 420 seconds (i.e. immunity effect on target)
- options to reduce delay to 6 or 30 seconds, or keep unchanged
- the 3rd option (no change) will patch effects if a related tweak from OlvynTweaks is detected

Uncap Crippling Strike
- allows Crippling Strike to scale to -16 (Assassin at level 50)
- by default, the stat reduction is capped at -7 (EE v2.5 and v2.6.6)
- the dialogue box and Record screen could show higher numbers, but the effect never went past -7
- main purpose is to allow Assassins to actually reach -10 in IWD:EE


==================================================
Fix weapon styles for some kits (mod-specific)
==================================================
- installable for: Rogue Rebalancing by aVENGER
                   3.5e Weapon Style Rebalance by Reddbane
- these tweaks raise max slots for certain kits that probably shouldn't get the boost
- currently affects 4 archer Thief kits and Loremaster (from Might and Guile)


==================================================
Weapon Style tweak for Deities of Faerun (EEs)
==================================================
- allows base-game Druid/Shaman kits to place 2 slots in Two-Weapon Style
- this just brings them up to the level of Raduziel's own divine kits (including from I Hate Undead kitpack)
- also affects a few mod-added kits (need to be added individually)


==================================================
Allow Minsc to use Berserk at will (BG games)
==================================================
- can set duration to 30, 60, or 120 seconds
- the way it works differs by game:
	- EEs: can be recast at any time (stat bonuses do not stack)
	- BG1: regain ability after duration runs out
	- BG2: regain ability immediately, but cannot recast until duration runs out
- BG2EE: fixes a timing error, which caused Minsc to always take 15 damage to his normal HP pool
- BG2: fixes incorrect durations for some effects (checked with fixpack v13)

NOTE: Will be skipped if Rashemi Berserker (Artisan's Kitpack) is installed


==================================================
Patch visuals for weapon types (game-specific)
==================================================
- IWDEE: Patch shortbows to use shortbow appearance (as in classic IWD)
- IWD-in-BG2: Patch scimitars to use scimitar appearance (was long sword)

NOTE: Shortbow appearance can't be set for IWD-in-BG2


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

On a technical level, this is a global script that runs once per character per game. It can theoretically take effect for games that are already started, but unless you're still at the beginning, you should have better equipment already.

Instructions:
- after installing, start a new game with new characters (you can also load one saved at the start)
- wait a few seconds for the script to run for each character
- that's it, the items will be either equipped or in the inventory
- for IWD1, if loading an existing save, you may need to open and close the Inventory or Record screen 1-2 times to make the script run


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
- to update the icon requires picking up and re-equipping each weapon (save/reload doesn't work)


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
- Rechargeable items: Amount gained when putting in the bag is always the same, regardless of number of charges left. Removing an item, however, seems to take into account the current charges. At 0 charges, an item is actually free to take back. So the exploit is obvious. You can deplete an item of charges, then continually add and remove the item from the bag to make infinite gold. Luckily, avoiding abusing the exploit is pretty easy. Just don't do it (unless you want to, of course). Resting will recharge any items with depleted charges, including in the bag.


==================================================
All classes get full HP from CON (classic and EEs)
==================================================
- yet another universal CON bonus mod
- choice between 2e/BG-style, or the more even HP curve of later editions
- usable with all versions of BG1, BG2, and IWD, including conversion mods


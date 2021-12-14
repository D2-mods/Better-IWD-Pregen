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

